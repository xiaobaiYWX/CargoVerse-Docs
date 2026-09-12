# Cargo 干线周转柜

制造商：云港物流集团 / Skyport Logistics

[返回制造商](<../README.md>) · [货柜目录](<../../README.md>)

面向区域集散与干线周转，以较低空重和制造费提高常规干货运输效率。

允许分类：农业产品（`agriculture`）、原始资源（`raw_resource`）、半成品资源（`processed_resource`）、精加工资源（`refined_resource`）、机械零件（`mechanical_parts`）、建筑材料（`construction_material`）、日常通用补给（`general_supplies`）。未列出的分类均不允许。

消除的运输要求：无。设计缺陷：无。所有货物的限时要求继续生效；御寒不代表冷藏或延长保质期。

| 货柜定义 | 资源 ID | 基础容量 t | 基础空重 Kpg | 基础耐久 | 调度点 | 规划加工费 VB | 结构状态 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [SPL Cargo 干线周转柜 M 型](<cargo_mc_m.md>) | `cargoverse:spl/cargo_mc_m` | 22 | 36 | 90 | 2 | 140 | 已提供正式模板 |
| [SPL Cargo 干线周转柜 L 型](<cargo_mc_l.md>) | `cargoverse:spl/cargo_mc_l` | 44 | 72 | 90 | 4 | 280 | 已提供正式模板 |

规划投放节点：区域集散港、干线物流站。加工费为 v3 目标，具体制造投放状态见各型号页；当前不新增贸易点与材料配方。
