# 深岩露天矿站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[D01 深岩露天矿站](<../../../07_贸易点/resource/深岩露天矿站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/sky_station/deepcore_mine` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/sky_station/deepcore_mine.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `hematite_ore` | [赤铁原矿](<../../../01_CargoGood/raw_resource/hematite_ore.md>) | `ingredient.raw_resource.hematite_ore` | 800 | 1600 | 400 | 0.95 |
| `copper_ore` | [含铜原矿](<../../../01_CargoGood/raw_resource/copper_ore.md>) | `ingredient.raw_resource.copper_ore` | 800 | 1600 | 400 | 0.95 |
| `quartz_sand` | [石英原砂](<../../../01_CargoGood/raw_resource/quartz_sand.md>) | `ingredient.raw_resource.quartz_sand` | 800 | 1600 | 400 | 0.95 |
| `stratigraphic_core_samples` | [地层岩芯](<../../../01_CargoGood/research_sample/stratigraphic_core_samples.md>) | `ingredient.research_sample.stratigraphic_core_samples` | 400 | 800 | 200 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 60 | 120 | 30 | 0.5 |
| `recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | `ingredient.processed_resource.recyclable_metal_scrap` | 60 | 120 | 30 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | false | 不限 | 1 |
| `ore_crushers` | [矿石破碎机](<../../../01_CargoGood/machinery/ore_crushers.md>) | `ingredient.machinery.ore_crushers` | true | 200 | 1.1 |
| `mining_haulers` | [矿用运输车](<../../../01_CargoGood/vehicle/mining_haulers.md>) | `ingredient.vehicle.mining_haulers` | false | 不限 | 1.1 |
| `mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | `ingredient.tools_equipment.mining_hand_tools` | false | 不限 | 1.1 |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | false | 不限 | 1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | false | 不限 | 1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | false | 不限 | 1 |
| `industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | `ingredient.chemical_material.industrial_lubricant` | false | 不限 | 1.05 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `hydraulic_cylinders` | [液压执行缸](<../../../01_CargoGood/mechanical_parts/hydraulic_cylinders.md>) | `ingredient.mechanical_parts.hydraulic_cylinders` | true | 100 | 1.05 |
| `industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | `ingredient.machinery.industrial_pump_sets` | true | 100 | 1.05 |
| `structural_steel_beams` | [标准钢梁](<../../../01_CargoGood/construction_material/structural_steel_beams.md>) | `ingredient.construction_material.structural_steel_beams` | true | 100 | 1.05 |

## 业务用途与维护

原矿与岩芯主供，扩大矿场机电维护需求；不把所有资源点都做成矿场，矿机、承重钢梁仍集中在本站。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/resource/深岩露天矿站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
