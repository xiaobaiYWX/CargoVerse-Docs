# 梯田农林站资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[V01 梯田农林站](<../../../07_贸易点/resource/agriculture/梯田农林站.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/agriculture/terrace_farm` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/agriculture/terrace_farm.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `bagged_wheat` | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | `ingredient.agriculture.bagged_wheat` | 6 | 18 | 6 | 常规周转 |
| `cotton_bales` | [纤维棉包](<../../../01_CargoGood/agriculture/cotton_bales.md>) | `ingredient.agriculture.cotton_bales` | 8 | 24 | 8 | 常规周转 |
| `greenhouse_fruit` | [温室鲜果](<../../../01_CargoGood/agriculture/greenhouse_fruit.md>) | `ingredient.agriculture.greenhouse_fruit` | 4 | 12 | 4 | 常规周转 |
| `hydroponic_leafy_greens` | [水培叶菜](<../../../01_CargoGood/agriculture/hydroponic_leafy_greens.md>) | `ingredient.agriculture.hydroponic_leafy_greens` | 4 | 12 | 4 | 常规周转 |
| `sealed_seed_grain` | [密封种粮](<../../../01_CargoGood/agriculture/sealed_seed_grain.md>) | `ingredient.agriculture.sealed_seed_grain` | 4 | 12 | 4 | 常规周转 |
| `industrial_cotton_cloth` | [工业棉布](<../../../01_CargoGood/processed_resource/industrial_cotton_cloth.md>) | `ingredient.processed_resource.industrial_cotton_cloth` | 4 | 12 | 4 | 常规周转 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | 4 | 12 | 4 | 常规周转 |
| `conifer_logs` | [针叶原木](<../../../01_CargoGood/raw_resource/conifer_logs.md>) | `ingredient.raw_resource.conifer_logs` | 8 | 24 | 8 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `tempered_glass_panels` | [钢化玻璃板](<../../../01_CargoGood/construction_material/tempered_glass_panels.md>) | `ingredient.construction_material.tempered_glass_panels` | 0 | 8.25 | 2.75 | false | 常规周转 |
| `greenhouse_frame_modules` | [温室骨架模块](<../../../01_CargoGood/prefab_structure/greenhouse_frame_modules.md>) | `ingredient.prefab_structure.greenhouse_frame_modules` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `breeding_poultry` | [家禽种群](<../../../01_CargoGood/livestock/breeding_poultry.md>) | `ingredient.livestock.breeding_poultry` | 0 | 6 | 2 | false | 常规周转 |
| `breeding_sheep` | [育成绵羊](<../../../01_CargoGood/livestock/breeding_sheep.md>) | `ingredient.livestock.breeding_sheep` | 0 | 6 | 2 | false | 常规周转 |
| `pollinator_colonies` | [授粉蜂群](<../../../01_CargoGood/livestock/pollinator_colonies.md>) | `ingredient.livestock.pollinator_colonies` | 0 | 6 | 2 | false | 常规周转 |
| `closed_loop_hydroponic_modules` | [循环水培舱](<../../../01_CargoGood/prefab_structure/closed_loop_hydroponic_modules.md>) | `ingredient.prefab_structure.closed_loop_hydroponic_modules` | 0 | 3 | 0.5 | false | 常规周转 |
| `hydroponic_nutrient_solution` | [水培营养液](<../../../01_CargoGood/chemical_material/hydroponic_nutrient_solution.md>) | `ingredient.chemical_material.hydroponic_nutrient_solution` | 0 | 11.25 | 3.75 | false | 常规周转 |
| `compound_fertilizer` | [复合肥料](<../../../01_CargoGood/chemical_material/compound_fertilizer.md>) | `ingredient.chemical_material.compound_fertilizer` | 0 | 12 | 4 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
