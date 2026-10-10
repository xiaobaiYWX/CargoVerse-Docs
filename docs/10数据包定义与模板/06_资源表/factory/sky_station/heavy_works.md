# 重工材料与矿机厂资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[D03 重工材料与矿机厂](<../../../07_贸易点/factory/重工材料与矿机厂/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/sky_station/heavy_works` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/sky_station/heavy_works.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补对应 `initial`、`capacity`、`daily_restock`。价格倍率作用于基础价值，整笔结算后取整。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:refined_resource/structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:refined_resource/precision_copper_wire` | [精密铜线](<../../../01_CargoGood/refined_resource/precision_copper_wire.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:machinery/ore_crushers` | [矿石破碎机](<../../../01_CargoGood/machinery/ore_crushers.md>) | 100 | 200 | 50 | 0.95 |
| `cargoverse:vehicle/mining_haulers` | [矿用运输车](<../../../01_CargoGood/vehicle/mining_haulers.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:tools_equipment/mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:special_resource/amethyst_resonator_plates` | [紫水晶谐振片](<../../../01_CargoGood/special_resource/amethyst_resonator_plates.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:valuables/cut_gemstones` | [切磨宝石](<../../../01_CargoGood/valuables/cut_gemstones.md>) | 100 | 200 | 50 | 0.95 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 100 | 200 | 50 | 0.95 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 100 | 200 | 50 | 1 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 60 | 120 | 30 | 0.5 |

## 收购 acquisitions

收购不建库存。填写 `daily_limit` 表示启用每日限额；省略时表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；`price_multiplier` 对该商品独立生效。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:machinery/precision_machine_tools` | [精密机床](<../../../01_CargoGood/machinery/precision_machine_tools.md>) | 200 | 1.1 |
| `cargoverse:mechanical_parts/hydraulic_cylinders` | [液压执行缸](<../../../01_CargoGood/mechanical_parts/hydraulic_cylinders.md>) | 不限 | 1.1 |
| `cargoverse:mechanical_parts/transmission_gears` | [标准传动齿轮](<../../../01_CargoGood/mechanical_parts/transmission_gears.md>) | 不限 | 1.1 |
| `cargoverse:processed_resource/iron_concentrate` | [铁精矿](<../../../01_CargoGood/processed_resource/iron_concentrate.md>) | 不限 | 1.1 |
| `cargoverse:processed_resource/copper_concentrate` | [铜精矿](<../../../01_CargoGood/processed_resource/copper_concentrate.md>) | 不限 | 1.1 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 不限 | 1 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 不限 | 1 |
| `cargoverse:medical_supply/first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | 不限 | 1 |
| `cargoverse:general_supplies/civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 不限 | 1 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 100 | 1.05 |
| `cargoverse:tools_equipment/precision_measuring_instruments` | [精密测量仪](<../../../01_CargoGood/tools_equipment/precision_measuring_instruments.md>) | 100 | 1.05 |
| `cargoverse:chemical_material/sealing_resin` | [密封树脂](<../../../01_CargoGood/chemical_material/sealing_resin.md>) | 不限 | 1.05 |
| `cargoverse:processed_resource/recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 不限 | 1.1 |

## 业务用途与维护

重工业与矿机主供，同时承担普通金属回收、矿务劳保和润滑油经销，连接生活补给、工业维护与采矿三类航线。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/factory/重工材料与矿机厂/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
