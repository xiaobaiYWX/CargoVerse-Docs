# 绿洲生物工程站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[V03 绿洲生物工程站](<../../../07_贸易点/factory/绿洲生物工程站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/sky_station/biosystems_station` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/sky_station/biosystems_station.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | 400 | 800 | 200 | 0.9 |
| `regenerative_culture_fluid` | [再生培养液](<../../../01_CargoGood/medical_supply/regenerative_culture_fluid.md>) | `ingredient.medical_supply.regenerative_culture_fluid` | 100 | 200 | 50 | 0.95 |
| `sterile_dressings` | [无菌敷料](<../../../01_CargoGood/medical_supply/sterile_dressings.md>) | `ingredient.medical_supply.sterile_dressings` | 200 | 400 | 100 | 0.95 |
| `vaccine_preparations` | [疫苗制剂](<../../../01_CargoGood/medical_supply/vaccine_preparations.md>) | `ingredient.medical_supply.vaccine_preparations` | 200 | 400 | 100 | 0.95 |
| `closed_loop_hydroponic_modules` | [循环水培舱](<../../../01_CargoGood/prefab_structure/closed_loop_hydroponic_modules.md>) | `ingredient.prefab_structure.closed_loop_hydroponic_modules` | 100 | 200 | 50 | 0.95 |
| `culture_medium` | [培养基原液](<../../../01_CargoGood/chemical_material/culture_medium.md>) | `ingredient.chemical_material.culture_medium` | 400 | 800 | 200 | 0.95 |
| `hydroponic_nutrient_solution` | [水培营养液](<../../../01_CargoGood/chemical_material/hydroponic_nutrient_solution.md>) | `ingredient.chemical_material.hydroponic_nutrient_solution` | 800 | 1600 | 400 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 60 | 120 | 30 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `cotton_bales` | [纤维棉包](<../../../01_CargoGood/agriculture/cotton_bales.md>) | `ingredient.agriculture.cotton_bales` | false | 不限 | 1.1 |
| `hatchery_fry` | [养殖鱼苗](<../../../01_CargoGood/livestock/hatchery_fry.md>) | `ingredient.livestock.hatchery_fry` | false | 不限 | 1.15 |
| `upper_air_microbe_samples` | [高空微生物样本](<../../../01_CargoGood/research_sample/upper_air_microbe_samples.md>) | `ingredient.research_sample.upper_air_microbe_samples` | false | 不限 | 1.15 |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | false | 不限 | 1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | false | 不限 | 1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | `ingredient.machinery.industrial_pump_sets` | true | 100 | 1.05 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `industrial_sensors` | [工业传感器](<../../../01_CargoGood/electronics/industrial_sensors.md>) | `ingredient.electronics.industrial_sensors` | true | 100 | 1.05 |
| `optical_glass_blanks` | [光学玻璃坯](<../../../01_CargoGood/refined_resource/optical_glass_blanks.md>) | `ingredient.refined_resource.optical_glass_blanks` | false | 不限 | 1.05 |
| `dried_organic_residue` | [干化有机废料](<../../../01_CargoGood/processed_resource/dried_organic_residue.md>) | `ingredient.processed_resource.dried_organic_residue` | false | 不限 | 1.1 |

## 业务用途与维护

医疗与生态设备主供、干化有机回收的重点买方；普通急救覆盖各行业，疫苗和再生培养液保留专门目的地。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/factory/绿洲生物工程站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
