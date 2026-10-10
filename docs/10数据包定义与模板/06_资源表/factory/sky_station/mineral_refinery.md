# 矿物分选精炼站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[D02 矿物分选精炼站](<../../../07_贸易点/factory/矿物分选精炼站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/sky_station/mineral_refinery` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/sky_station/mineral_refinery.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补对应 `initial`、`capacity`、`daily_restock`。价格倍率作用于基础价值，整笔结算后取整。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:processed_resource/iron_concentrate` | [铁精矿](<../../../01_CargoGood/processed_resource/iron_concentrate.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:processed_resource/copper_concentrate` | [铜精矿](<../../../01_CargoGood/processed_resource/copper_concentrate.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:hazardous_material/heavy_metal_filter_cake` | [重金属滤渣](<../../../01_CargoGood/hazardous_material/heavy_metal_filter_cake.md>) | 800 | 1600 | 400 | 0.5 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 60 | 120 | 30 | 0.5 |
| `cargoverse:processed_resource/recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 60 | 120 | 30 | 0.5 |

## 收购 acquisitions

收购不建库存。填写 `daily_limit` 表示启用每日限额；省略时表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；`price_multiplier` 对该商品独立生效。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:raw_resource/hematite_ore` | [赤铁原矿](<../../../01_CargoGood/raw_resource/hematite_ore.md>) | 不限 | 1.1 |
| `cargoverse:raw_resource/copper_ore` | [含铜原矿](<../../../01_CargoGood/raw_resource/copper_ore.md>) | 不限 | 1.1 |
| `cargoverse:energy_fuel/coke_fuel` | [煤焦燃料](<../../../01_CargoGood/energy_fuel/coke_fuel.md>) | 不限 | 1.1 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 不限 | 1 |
| `cargoverse:medical_supply/first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | 不限 | 1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 不限 | 1 |
| `cargoverse:general_supplies/civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 不限 | 1 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 不限 | 1.05 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 100 | 1.05 |
| `cargoverse:mechanical_parts/transmission_gears` | [标准传动齿轮](<../../../01_CargoGood/mechanical_parts/transmission_gears.md>) | 100 | 1.05 |
| `cargoverse:electronics/industrial_sensors` | [工业传感器](<../../../01_CargoGood/electronics/industrial_sensors.md>) | 100 | 1.05 |
| `cargoverse:machinery/industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | 100 | 1.05 |
| `cargoverse:refined_resource/structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | 不限 | 1.05 |

## 业务用途与维护

保持原矿到精矿的贸易背景，接收泵、齿轮与传感器等维护物资；为恶地和岩质丘陵矿场经销口粮，补齐当地生活补给来源。普通边角料与专用危废分开出售，收购不触发实际精炼。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/factory/矿物分选精炼站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
