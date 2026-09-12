# 重工材料与矿机厂资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[D03 重工材料与矿机厂](<../../../07_贸易点/factory/heavy/重工材料与矿机厂.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/heavy/heavy_works` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/heavy/heavy_works.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | `ingredient.refined_resource.structural_steel_ingots` | 2 | 6 | 2 | 常规周转 |
| `precision_copper_wire` | [精密铜线](<../../../01_CargoGood/refined_resource/precision_copper_wire.md>) | `ingredient.refined_resource.precision_copper_wire` | 2 | 6 | 2 | 常规周转 |
| `ore_crushers` | [矿石破碎机](<../../../01_CargoGood/machinery/ore_crushers.md>) | `ingredient.machinery.ore_crushers` | 1 | 3 | 1 | 常规周转 |
| `mining_haulers` | [矿用运输车](<../../../01_CargoGood/vehicle/mining_haulers.md>) | `ingredient.vehicle.mining_haulers` | 2 | 6 | 2 | 常规周转 |
| `mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | `ingredient.tools_equipment.mining_hand_tools` | 4 | 12 | 4 | 常规周转 |
| `amethyst_resonator_plates` | [紫水晶谐振片](<../../../01_CargoGood/special_resource/amethyst_resonator_plates.md>) | `ingredient.special_resource.amethyst_resonator_plates` | 2 | 6 | 2 | 常规周转 |
| `cut_gemstones` | [切磨宝石](<../../../01_CargoGood/valuables/cut_gemstones.md>) | `ingredient.valuables.cut_gemstones` | 1 | 3 | 1 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `precision_machine_tools` | [精密机床](<../../../01_CargoGood/machinery/precision_machine_tools.md>) | `ingredient.machinery.precision_machine_tools` | 0 | 3 | 1 | false | 常规周转 |
| `hydraulic_cylinders` | [液压执行缸](<../../../01_CargoGood/mechanical_parts/hydraulic_cylinders.md>) | `ingredient.mechanical_parts.hydraulic_cylinders` | 0 | 6 | 2 | false | 常规周转 |
| `transmission_gears` | [标准传动齿轮](<../../../01_CargoGood/mechanical_parts/transmission_gears.md>) | `ingredient.mechanical_parts.transmission_gears` | 0 | 6 | 2 | false | 常规周转 |
| `iron_concentrate` | [铁精矿](<../../../01_CargoGood/processed_resource/iron_concentrate.md>) | `ingredient.processed_resource.iron_concentrate` | 0 | 12 | 4 | false | 常规周转 |
| `copper_concentrate` | [铜精矿](<../../../01_CargoGood/processed_resource/copper_concentrate.md>) | `ingredient.processed_resource.copper_concentrate` | 0 | 12 | 4 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
