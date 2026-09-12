# 标准建材装配港资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[A01 标准建材装配港](<../../../07_贸易点/factory/construction/标准建材装配港.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/construction/standard_assembly` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/construction/standard_assembly.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `bagged_cement` | [袋装水泥](<../../../01_CargoGood/construction_material/bagged_cement.md>) | `ingredient.construction_material.bagged_cement` | 8 | 24 | 8 | 常规周转 |
| `insulation_panels` | [保温板材](<../../../01_CargoGood/construction_material/insulation_panels.md>) | `ingredient.construction_material.insulation_panels` | 2 | 6 | 2 | 常规周转 |
| `structural_steel_beams` | [标准钢梁](<../../../01_CargoGood/construction_material/structural_steel_beams.md>) | `ingredient.construction_material.structural_steel_beams` | 2 | 6 | 2 | 常规周转 |
| `tempered_glass_panels` | [钢化玻璃板](<../../../01_CargoGood/construction_material/tempered_glass_panels.md>) | `ingredient.construction_material.tempered_glass_panels` | 4 | 12 | 4 | 常规周转 |
| `prefab_habitat_pods` | [预制居住舱](<../../../01_CargoGood/prefab_structure/prefab_habitat_pods.md>) | `ingredient.prefab_structure.prefab_habitat_pods` | 2 | 6 | 2 | 常规周转 |
| `greenhouse_frame_modules` | [温室骨架模块](<../../../01_CargoGood/prefab_structure/greenhouse_frame_modules.md>) | `ingredient.prefab_structure.greenhouse_frame_modules` | 2 | 6 | 2 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `quartz_sand` | [石英原砂](<../../../01_CargoGood/raw_resource/quartz_sand.md>) | `ingredient.raw_resource.quartz_sand` | 0 | 36 | 12 | false | 常规周转 |
| `structural_steel_ingots` | [结构钢锭](<../../../01_CargoGood/refined_resource/structural_steel_ingots.md>) | `ingredient.refined_resource.structural_steel_ingots` | 0 | 4.5 | 1.5 | false | 常规周转 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | 0 | 18 | 6 | false | 常规周转 |
| `sealing_resin` | [密封树脂](<../../../01_CargoGood/chemical_material/sealing_resin.md>) | `ingredient.chemical_material.sealing_resin` | 0 | 9 | 3 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
