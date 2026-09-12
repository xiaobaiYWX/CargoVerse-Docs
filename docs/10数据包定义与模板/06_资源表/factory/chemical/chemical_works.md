# 工业化学品供应站资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[E02 工业化学品供应站](<../../../07_贸易点/factory/chemical/工业化学品供应站.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/chemical/chemical_works` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/chemical/chemical_works.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `compound_fertilizer` | [复合肥料](<../../../01_CargoGood/chemical_material/compound_fertilizer.md>) | `ingredient.chemical_material.compound_fertilizer` | 8 | 24 | 8 | 常规周转 |
| `industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | `ingredient.chemical_material.industrial_lubricant` | 8 | 24 | 8 | 常规周转 |
| `sealing_resin` | [密封树脂](<../../../01_CargoGood/chemical_material/sealing_resin.md>) | `ingredient.chemical_material.sealing_resin` | 4 | 12 | 4 | 常规周转 |
| `glowstone_luminant` | [萤石发光粉](<../../../01_CargoGood/special_resource/glowstone_luminant.md>) | `ingredient.special_resource.glowstone_luminant` | 4 | 12 | 4 | 常规周转 |
| `nether_quartz_clusters` | [下界石英晶簇](<../../../01_CargoGood/special_resource/nether_quartz_clusters.md>) | `ingredient.special_resource.nether_quartz_clusters` | 2 | 6 | 2 | 常规周转 |
| `spent_acid_drums` | [废酸回收桶](<../../../01_CargoGood/hazardous_material/spent_acid_drums.md>) | `ingredient.hazardous_material.spent_acid_drums` | 8 | 24 | 8 | 常规周转 |

## 收购 acquisitions

空数组 `[]`，本节点不收购 CargoGood。

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
