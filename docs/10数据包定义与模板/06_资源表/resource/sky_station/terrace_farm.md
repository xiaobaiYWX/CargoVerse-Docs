# 梯田农林站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[V01 梯田农林站](<../../../07_贸易点/resource/梯田农林站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/sky_station/terrace_farm` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/sky_station/terrace_farm.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补对应 `initial`、`capacity`、`daily_restock`。价格倍率作用于基础价值，整笔结算后取整。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:agriculture/bagged_wheat` | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | 600 | 1200 | 300 | 0.95 |
| `cargoverse:agriculture/cotton_bales` | [纤维棉包](<../../../01_CargoGood/agriculture/cotton_bales.md>) | 800 | 1600 | 400 | 0.95 |
| `cargoverse:agriculture/greenhouse_fruit` | [温室鲜果](<../../../01_CargoGood/agriculture/greenhouse_fruit.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:agriculture/hydroponic_leafy_greens` | [水培叶菜](<../../../01_CargoGood/agriculture/hydroponic_leafy_greens.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:agriculture/sealed_seed_grain` | [密封种粮](<../../../01_CargoGood/agriculture/sealed_seed_grain.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:processed_resource/industrial_cotton_cloth` | [工业棉布](<../../../01_CargoGood/processed_resource/industrial_cotton_cloth.md>) | 400 | 800 | 200 | 0.95 |
| `cargoverse:processed_resource/kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 400 | 800 | 200 | 0.9 |
| `cargoverse:raw_resource/conifer_logs` | [针叶原木](<../../../01_CargoGood/raw_resource/conifer_logs.md>) | 800 | 1600 | 400 | 0.95 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 60 | 120 | 30 | 0.5 |
| `cargoverse:processed_resource/dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | 80 | 160 | 40 | 0.5 |

## 收购 acquisitions

收购不建库存。填写 `daily_limit` 表示启用每日限额；省略时表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；`price_multiplier` 对该商品独立生效。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:construction_material/tempered_glass_panels` | [钢化玻璃板](<../../../01_CargoGood/construction_material/tempered_glass_panels.md>) | 不限 | 1.1 |
| `cargoverse:prefab_structure/greenhouse_frame_modules` | [温室骨架模块](<../../../01_CargoGood/prefab_structure/greenhouse_frame_modules.md>) | 不限 | 1.1 |
| `cargoverse:livestock/breeding_poultry` | [家禽种群](<../../../01_CargoGood/livestock/breeding_poultry.md>) | 不限 | 1.15 |
| `cargoverse:livestock/breeding_sheep` | [育成绵羊](<../../../01_CargoGood/livestock/breeding_sheep.md>) | 不限 | 1.15 |
| `cargoverse:livestock/pollinator_colonies` | [授粉蜂群](<../../../01_CargoGood/livestock/pollinator_colonies.md>) | 不限 | 1.15 |
| `cargoverse:prefab_structure/closed_loop_hydroponic_modules` | [循环水培舱](<../../../01_CargoGood/prefab_structure/closed_loop_hydroponic_modules.md>) | 200 | 1.15 |
| `cargoverse:chemical_material/hydroponic_nutrient_solution` | [水培营养液](<../../../01_CargoGood/chemical_material/hydroponic_nutrient_solution.md>) | 不限 | 1.1 |
| `cargoverse:chemical_material/compound_fertilizer` | [复合肥料](<../../../01_CargoGood/chemical_material/compound_fertilizer.md>) | 不限 | 1.1 |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 不限 | 1 |
| `cargoverse:medical_supply/first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | 不限 | 1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 不限 | 1 |
| `cargoverse:general_supplies/civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 不限 | 1 |
| `cargoverse:machinery/industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | 100 | 1.05 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 不限 | 1.05 |
| `cargoverse:energy_fuel/industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | 100 | 1.05 |
| `cargoverse:tools_equipment/mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 不限 | 1.05 |
| `cargoverse:energy_fuel/biomass_briquettes` | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | 不限 | 1.05 |

## 业务用途与维护

农林综合来源，新增自产常温口粮；泵、能源与手工具构成普遍农业设备需求，温室和育种货物保留原重点收购。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/resource/梯田农林站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
