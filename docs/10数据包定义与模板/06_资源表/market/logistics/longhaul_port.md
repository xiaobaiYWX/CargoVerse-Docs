# 远航货运枢纽资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[S02 远航货运枢纽](<../../../07_贸易点/market/logistics/远航货运枢纽.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/logistics/longhaul_port` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/logistics/longhaul_port.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

空数组 `[]`，本节点首版不出售 CargoGood。

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `bagged_cement` | [袋装水泥](<../../../01_CargoGood/construction_material/bagged_cement.md>) | `ingredient.construction_material.bagged_cement` | 0 | 36.75 | 12.25 | false | 常规周转 |
| `insulation_panels` | [保温板材](<../../../01_CargoGood/construction_material/insulation_panels.md>) | `ingredient.construction_material.insulation_panels` | 0 | 9.75 | 3.25 | false | 常规周转 |
| `structural_steel_beams` | [标准钢梁](<../../../01_CargoGood/construction_material/structural_steel_beams.md>) | `ingredient.construction_material.structural_steel_beams` | 0 | 9.75 | 3.25 | false | 常规周转 |
| `automated_cargo_handlers` | [自动装卸机](<../../../01_CargoGood/machinery/automated_cargo_handlers.md>) | `ingredient.machinery.automated_cargo_handlers` | 0 | 3 | 1 | false | 常规周转 |
| `airship_keel_modules` | [飞艇龙骨模块](<../../../01_CargoGood/prefab_structure/airship_keel_modules.md>) | `ingredient.prefab_structure.airship_keel_modules` | 0 | 3 | 0.75 | false | 常规周转 |
| `propulsion_impellers` | [推进器叶轮](<../../../01_CargoGood/mechanical_parts/propulsion_impellers.md>) | `ingredient.mechanical_parts.propulsion_impellers` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `avionics_controllers` | [航电控制器](<../../../01_CargoGood/electronics/avionics_controllers.md>) | `ingredient.electronics.avionics_controllers` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `port_tractors` | [港区牵引车](<../../../01_CargoGood/vehicle/port_tractors.md>) | `ingredient.vehicle.port_tractors` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `aviation_maintenance_toolkits` | [航修工具箱](<../../../01_CargoGood/tools_equipment/aviation_maintenance_toolkits.md>) | `ingredient.tools_equipment.aviation_maintenance_toolkits` | 0 | 4.5 | 1.5 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
