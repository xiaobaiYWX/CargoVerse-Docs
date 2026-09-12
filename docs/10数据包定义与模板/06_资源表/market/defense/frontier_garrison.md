# 边境驻防补给港资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[B03 边境驻防补给港](<../../../07_贸易点/market/defense/边境驻防补给港.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/defense/frontier_garrison` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/defense/frontier_garrison.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

空数组 `[]`，本节点首版不出售 CargoGood。

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 0 | 36 | 12 | false | 常规周转 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | 0 | 9 | 3 | false | 常规周转 |
| `sterile_dressings` | [无菌敷料](<../../../01_CargoGood/medical_supply/sterile_dressings.md>) | `ingredient.medical_supply.sterile_dressings` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `vaccine_preparations` | [疫苗制剂](<../../../01_CargoGood/medical_supply/vaccine_preparations.md>) | `ingredient.medical_supply.vaccine_preparations` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `garrison_ammunition_crates` | [驻防弹药箱](<../../../01_CargoGood/weapon_armor/garrison_ammunition_crates.md>) | `ingredient.weapon_armor.garrison_ammunition_crates` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `guard_armor` | [护卫护甲](<../../../01_CargoGood/weapon_armor/guard_armor.md>) | `ingredient.weapon_armor.guard_armor` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `service_crossbows` | [制式弩机](<../../../01_CargoGood/weapon_armor/service_crossbows.md>) | `ingredient.weapon_armor.service_crossbows` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `ship_defense_gun_sets` | [舰载防御炮组](<../../../01_CargoGood/weapon_armor/ship_defense_gun_sets.md>) | `ingredient.weapon_armor.ship_defense_gun_sets` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `perimeter_security_systems` | [周界警戒系统](<../../../01_CargoGood/electronics/perimeter_security_systems.md>) | `ingredient.electronics.perimeter_security_systems` | 0 | 3 | 1 | false | 常规周转 |
| `prefab_defensive_positions` | [预制防御工事](<../../../01_CargoGood/prefab_structure/prefab_defensive_positions.md>) | `ingredient.prefab_structure.prefab_defensive_positions` | 0 | 3 | 1 | false | 常规周转 |
| `light_patrol_boats` | [轻型巡逻艇](<../../../01_CargoGood/vehicle/light_patrol_boats.md>) | `ingredient.vehicle.light_patrol_boats` | 0 | 3 | 1 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
