# 远航货运枢纽资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[S02 远航货运枢纽](<../../../07_贸易点/market/远航货运枢纽/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/sky_station/longhaul_port` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/sky_station/longhaul_port.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 400 | 800 | 200 | 0.95 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | 400 | 800 | 200 | 0.95 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | 200 | 400 | 100 | 0.95 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | 200 | 400 | 100 | 0.95 |
| `industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | `ingredient.chemical_material.industrial_lubricant` | 100 | 200 | 50 | 1 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | 100 | 200 | 50 | 1 |
| `aviation_fuel_drums` | [桶装航空燃油](<../../../01_CargoGood/energy_fuel/aviation_fuel_drums.md>) | `ingredient.energy_fuel.aviation_fuel_drums` | 200 | 400 | 100 | 1 |
| `recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | `ingredient.processed_resource.recyclable_metal_scrap` | 60 | 120 | 30 | 0.5 |
| `scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | `ingredient.mechanical_parts.scrapped_electronic_components` | 40 | 80 | 20 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `bagged_cement` | [袋装水泥](<../../../01_CargoGood/construction_material/bagged_cement.md>) | `ingredient.construction_material.bagged_cement` | false | 不限 | 1.1 |
| `insulation_panels` | [保温板材](<../../../01_CargoGood/construction_material/insulation_panels.md>) | `ingredient.construction_material.insulation_panels` | false | 不限 | 1.1 |
| `structural_steel_beams` | [标准钢梁](<../../../01_CargoGood/construction_material/structural_steel_beams.md>) | `ingredient.construction_material.structural_steel_beams` | false | 不限 | 1.1 |
| `automated_cargo_handlers` | [自动装卸机](<../../../01_CargoGood/machinery/automated_cargo_handlers.md>) | `ingredient.machinery.automated_cargo_handlers` | true | 200 | 1.1 |
| `airship_keel_modules` | [飞艇龙骨模块](<../../../01_CargoGood/prefab_structure/airship_keel_modules.md>) | `ingredient.prefab_structure.airship_keel_modules` | true | 200 | 1.15 |
| `propulsion_impellers` | [推进器叶轮](<../../../01_CargoGood/mechanical_parts/propulsion_impellers.md>) | `ingredient.mechanical_parts.propulsion_impellers` | false | 不限 | 1.15 |
| `avionics_controllers` | [航电控制器](<../../../01_CargoGood/electronics/avionics_controllers.md>) | `ingredient.electronics.avionics_controllers` | false | 不限 | 1.15 |
| `port_tractors` | [港区牵引车](<../../../01_CargoGood/vehicle/port_tractors.md>) | `ingredient.vehicle.port_tractors` | false | 不限 | 1.1 |
| `aviation_maintenance_toolkits` | [航修工具箱](<../../../01_CargoGood/tools_equipment/aviation_maintenance_toolkits.md>) | `ingredient.tools_equipment.aviation_maintenance_toolkits` | false | 不限 | 1.1 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | false | 不限 | 1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `standard_container_couplings` | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | `ingredient.mechanical_parts.standard_container_couplings` | true | 100 | 1.05 |
| `precision_bearings` | [精密轴承](<../../../01_CargoGood/mechanical_parts/precision_bearings.md>) | `ingredient.mechanical_parts.precision_bearings` | true | 100 | 1.05 |
| `hydraulic_cylinders` | [液压执行缸](<../../../01_CargoGood/mechanical_parts/hydraulic_cylinders.md>) | `ingredient.mechanical_parts.hydraulic_cylinders` | true | 100 | 1.05 |
| `tempered_glass_panels` | [钢化玻璃板](<../../../01_CargoGood/construction_material/tempered_glass_panels.md>) | `ingredient.construction_material.tempered_glass_panels` | false | 不限 | 1.05 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | false | 不限 | 1 |

## 业务用途与维护

从纯重装收购港转为备航集散中心，出售口粮、净水、急救、木板及设备油料；经销价高于主供站，保留专程寻找生产地的价值。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/market/远航货运枢纽/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
