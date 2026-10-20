# Atlas 标准干货柜

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。

制造商：天穹联合工业 / Aether Union Industries

[返回制造商](<../README.md>) · [货柜目录](<../../README.md>)

面向跨行业基础运输，提供广泛的干货兼容性、可靠防护与标准化维护。

允许分类：农业物资（`agriculture`）、食品与食材（`food`）、原料资源（`raw_resource`）、加工材料（`processed_resource`）、机械零件（`mechanical_parts`）、建筑构件（`construction_material`）、物流与仓储（`logistics_equipment`）、通用物资（`general_supplies`）、工具与装备（`tools_equipment`）。分类按 2026-10-20 的十四类方案更新，未列出分类不允许。

消除的运输要求：无。设计缺陷：无。所有货物的限时要求继续生效；御寒不代表冷藏或延长保质期。

| 货柜定义 | 资源 ID | 基础容量（个） | 基础空重 Kpg | 基础耐久 | 调度点 | v2 加工费 VB | 结构状态 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [AUI Atlas 标准干货柜 S 型](<atlas_sd_s.md>) | `cargoverse:aui/atlas_sd_s` | 50 | 20 | 100 | 1 | 80 | 已提供正式模板 |
| [AUI Atlas 标准干货柜 M 型](<atlas_sd_m.md>) | `cargoverse:aui/atlas_sd_m` | 100 | 40 | 100 | 2 | 160 | 已提供正式模板 |
| [AUI Atlas 标准干货柜 L 型](<atlas_sd_l.md>) | `cargoverse:aui/atlas_sd_l` | 200 | 80 | 100 | 4 | 320 | 已提供正式模板 |
| [AUI Atlas 标准干货柜 X 型](<atlas_sd_x.md>) | `cargoverse:aui/atlas_sd_x` | 350 | 140 | 100 | 6 | 560 | 已提供正式模板 |

规划投放节点：综合港、独立运输者起步站。材料与加工费采用 v2 实体物品设计，具体投放状态见各型号页。

[统一实体配方与实际规划节点](<../../../08_货柜制造台/制造配方与投放总表.md>)：系列材料、加工费和门槛以当前型号页为准。
