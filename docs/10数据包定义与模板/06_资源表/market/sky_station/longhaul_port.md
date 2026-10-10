# 远航货运枢纽资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[S02 远航货运枢纽](<../../../07_贸易点/market/远航货运枢纽/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/sky_station/longhaul_port` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/sky_station/longhaul_port.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补对应 `initial`、`capacity`、`daily_restock`。价格倍率作用于基础价值，整笔结算后取整。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:medical_supply/first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:processed_resource/kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 100 | 200 | 50 | 1 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 100 | 200 | 50 | 1 |
| `cargoverse:energy_fuel/aviation_fuel_drums` | [桶装航空燃油](<../../../01_CargoGood/energy_fuel/aviation_fuel_drums.md>) | 200 | 400 | 100 | 1 |
| `cargoverse:processed_resource/recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 60 | 120 | 30 | 0.5 |
| `cargoverse:mechanical_parts/scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | 40 | 80 | 20 | 0.5 |

## 收购 acquisitions

收购不建库存。填写 `daily_limit` 表示启用每日限额；省略时表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；`price_multiplier` 对该商品独立生效。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:construction_material/bagged_cement` | [袋装水泥](<../../../01_CargoGood/construction_material/bagged_cement.md>) | 不限 | 1.1 |
| `cargoverse:construction_material/insulation_panels` | [保温板材](<../../../01_CargoGood/construction_material/insulation_panels.md>) | 不限 | 1.1 |
| `cargoverse:construction_material/structural_steel_beams` | [标准钢梁](<../../../01_CargoGood/construction_material/structural_steel_beams.md>) | 不限 | 1.1 |
| `cargoverse:machinery/automated_cargo_handlers` | [自动装卸机](<../../../01_CargoGood/machinery/automated_cargo_handlers.md>) | 200 | 1.1 |
| `cargoverse:prefab_structure/airship_keel_modules` | [飞艇龙骨模块](<../../../01_CargoGood/prefab_structure/airship_keel_modules.md>) | 200 | 1.15 |
| `cargoverse:mechanical_parts/propulsion_impellers` | [推进器叶轮](<../../../01_CargoGood/mechanical_parts/propulsion_impellers.md>) | 不限 | 1.15 |
| `cargoverse:electronics/avionics_controllers` | [航电控制器](<../../../01_CargoGood/electronics/avionics_controllers.md>) | 不限 | 1.15 |
| `cargoverse:vehicle/port_tractors` | [港区牵引车](<../../../01_CargoGood/vehicle/port_tractors.md>) | 不限 | 1.1 |
| `cargoverse:tools_equipment/aviation_maintenance_toolkits` | [航修工具箱](<../../../01_CargoGood/tools_equipment/aviation_maintenance_toolkits.md>) | 不限 | 1.1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 不限 | 1 |
| `cargoverse:general_supplies/civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 不限 | 1 |
| `cargoverse:mechanical_parts/standard_container_couplings` | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | 100 | 1.05 |
| `cargoverse:mechanical_parts/precision_bearings` | [精密轴承](<../../../01_CargoGood/mechanical_parts/precision_bearings.md>) | 100 | 1.05 |
| `cargoverse:mechanical_parts/hydraulic_cylinders` | [液压执行缸](<../../../01_CargoGood/mechanical_parts/hydraulic_cylinders.md>) | 100 | 1.05 |
| `cargoverse:construction_material/tempered_glass_panels` | [钢化玻璃板](<../../../01_CargoGood/construction_material/tempered_glass_panels.md>) | 不限 | 1.05 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 不限 | 1 |

## 业务用途与维护

从纯重装收购港转为备航集散中心，出售口粮、净水、急救、木板及设备油料；经销价高于主供站，保留专程寻找生产地的价值。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/market/远航货运枢纽/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
