# 绿洲生物工程站资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[V03 绿洲生物工程站](<../../../07_贸易点/factory/biology/绿洲生物工程站.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/biology/biosystems_station` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/biology/biosystems_station.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | 4 | 12 | 4 | 常规周转 |
| `regenerative_culture_fluid` | [再生培养液](<../../../01_CargoGood/medical_supply/regenerative_culture_fluid.md>) | `ingredient.medical_supply.regenerative_culture_fluid` | 1 | 3 | 1 | 常规周转 |
| `sterile_dressings` | [无菌敷料](<../../../01_CargoGood/medical_supply/sterile_dressings.md>) | `ingredient.medical_supply.sterile_dressings` | 2 | 6 | 2 | 常规周转 |
| `vaccine_preparations` | [疫苗制剂](<../../../01_CargoGood/medical_supply/vaccine_preparations.md>) | `ingredient.medical_supply.vaccine_preparations` | 2 | 6 | 2 | 常规周转 |
| `closed_loop_hydroponic_modules` | [循环水培舱](<../../../01_CargoGood/prefab_structure/closed_loop_hydroponic_modules.md>) | `ingredient.prefab_structure.closed_loop_hydroponic_modules` | 1 | 3 | 1 | 常规周转 |
| `culture_medium` | [培养基原液](<../../../01_CargoGood/chemical_material/culture_medium.md>) | `ingredient.chemical_material.culture_medium` | 4 | 12 | 4 | 常规周转 |
| `hydroponic_nutrient_solution` | [水培营养液](<../../../01_CargoGood/chemical_material/hydroponic_nutrient_solution.md>) | `ingredient.chemical_material.hydroponic_nutrient_solution` | 8 | 24 | 8 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `cotton_bales` | [纤维棉包](<../../../01_CargoGood/agriculture/cotton_bales.md>) | `ingredient.agriculture.cotton_bales` | 0 | 54.75 | 18.25 | false | 常规周转 |
| `hatchery_fry` | [养殖鱼苗](<../../../01_CargoGood/livestock/hatchery_fry.md>) | `ingredient.livestock.hatchery_fry` | 0 | 14.25 | 4.75 | false | 常规周转 |
| `upper_air_microbe_samples` | [高空微生物样本](<../../../01_CargoGood/research_sample/upper_air_microbe_samples.md>) | `ingredient.research_sample.upper_air_microbe_samples` | 0 | 6 | 2 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
