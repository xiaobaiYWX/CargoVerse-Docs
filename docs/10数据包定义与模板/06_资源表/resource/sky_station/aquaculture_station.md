# 云泽水产与育种站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[V02 云泽水产与育种站](<../../../07_贸易点/resource/云泽水产与育种站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/sky_station/aquaculture_station` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/sky_station/aquaculture_station.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补对应 `initial`、`capacity`、`daily_restock`。价格倍率作用于基础价值，整笔结算后取整。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:aquatic/chilled_river_fish` | [冰鲜河鱼](<../../../01_CargoGood/aquatic/chilled_river_fish.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:aquatic/chilled_sea_shrimp` | [冰鲜海虾](<../../../01_CargoGood/aquatic/chilled_sea_shrimp.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:aquatic/fresh_kelp` | [鲜采食用海带](<../../../01_CargoGood/aquatic/fresh_kelp.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:aquatic/purified_shellfish` | [净化鲜贝](<../../../01_CargoGood/aquatic/purified_shellfish.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:livestock/breeding_poultry` | [家禽种群](<../../../01_CargoGood/livestock/breeding_poultry.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:livestock/breeding_sheep` | [育成绵羊](<../../../01_CargoGood/livestock/breeding_sheep.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:livestock/hatchery_fry` | [养殖鱼苗](<../../../01_CargoGood/livestock/hatchery_fry.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:livestock/pollinator_colonies` | [授粉蜂群](<../../../01_CargoGood/livestock/pollinator_colonies.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 60 | 120 | 30 | 0.5 |
| `cargoverse:processed_resource/dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | 80 | 160 | 40 | 0.5 |

## 收购 acquisitions

收购不建库存。填写 `daily_limit` 表示启用每日限额；省略时表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；`price_multiplier` 对该商品独立生效。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:agriculture/sealed_seed_grain` | [密封种粮](<../../../01_CargoGood/agriculture/sealed_seed_grain.md>) | 不限 | 1.1 |
| `cargoverse:prefab_structure/containerized_water_stations` | [集装式净水站](<../../../01_CargoGood/prefab_structure/containerized_water_stations.md>) | 200 | 1.1 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 不限 | 1 |
| `cargoverse:medical_supply/first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | 不限 | 1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 不限 | 1 |
| `cargoverse:general_supplies/civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 不限 | 1 |
| `cargoverse:processed_resource/kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 不限 | 1 |
| `cargoverse:machinery/industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | 100 | 1.05 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 100 | 1.05 |
| `cargoverse:chemical_material/hydroponic_nutrient_solution` | [水培营养液](<../../../01_CargoGood/chemical_material/hydroponic_nutrient_solution.md>) | 不限 | 1.05 |

## 业务用途与维护

水产育种主供兼净水补给来源；泵与能源支撑养殖背景，鲜货和有机残料分别运往市场与生物／能源站。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/resource/云泽水产与育种站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
