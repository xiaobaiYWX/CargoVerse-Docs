# 云港民生集配站资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[S01 云港民生集配站](<../../../07_贸易点/market/logistics/云港民生集配站.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/logistics/civic_distribution` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/logistics/civic_distribution.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 8 | 24 | 8 | 常规周转 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | 2 | 6 | 2 | 常规周转 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | 2 | 6 | 2 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `prefab_habitat_pods` | [预制居住舱](<../../../01_CargoGood/prefab_structure/prefab_habitat_pods.md>) | `ingredient.prefab_structure.prefab_habitat_pods` | 0 | 5.25 | 1.75 | false | 常规周转 |
| `bagged_wheat` | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | `ingredient.agriculture.bagged_wheat` | 0 | 21 | 7 | false | 常规周转 |
| `industrial_cotton_cloth` | [工业棉布](<../../../01_CargoGood/processed_resource/industrial_cotton_cloth.md>) | `ingredient.processed_resource.industrial_cotton_cloth` | 0 | 14.25 | 4.75 | false | 常规周转 |
| `biomass_briquettes` | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | `ingredient.energy_fuel.biomass_briquettes` | 0 | 24 | 8 | false | 常规周转 |
| `glowstone_luminant` | [萤石发光粉](<../../../01_CargoGood/special_resource/glowstone_luminant.md>) | `ingredient.special_resource.glowstone_luminant` | 0 | 7.5 | 2.5 | false | 常规周转 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | 0 | 21 | 7 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
