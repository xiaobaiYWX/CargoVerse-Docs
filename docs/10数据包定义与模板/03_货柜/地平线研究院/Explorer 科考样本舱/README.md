# Explorer 科考样本舱

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。

制造商：地平线研究院 / Horizon Research Institute

[返回制造商](<../README.md>) · [货柜目录](<../../README.md>)

面向科考样本和采样器材往返，通过缓冲、防潮与遮光设计保护研究物资。

允许分类：原料资源（`raw_resource`）、加工材料（`processed_resource`）、工具与装备（`tools_equipment`）、化工与药剂（`chemical_material`）、红石与控制（`electronics`）、通用物资（`general_supplies`）。分类按 2026-10-20 的十四类方案更新，未列出分类不允许。

消除的运输要求：易碎、防潮、避光。设计缺陷：无。所有货物的限时要求继续生效；御寒不代表冷藏或延长保质期。

| 货柜定义 | 资源 ID | 基础容量（个） | 基础空重 Kpg | 基础耐久 | 调度点 | v2 加工费 VB | 结构状态 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [HRI Explorer 科考样本舱 S 型](<explorer_si_s.md>) | `cargoverse:hri/explorer_si_s` | 40 | 24 | 125 | 1 | 180 | 已提供正式模板 |
| [HRI Explorer 科考样本舱 M 型](<explorer_si_m.md>) | `cargoverse:hri/explorer_si_m` | 80 | 48 | 125 | 2 | 360 | 已提供正式模板 |
| [HRI Explorer 科考样本舱 L 型](<explorer_si_l.md>) | `cargoverse:hri/explorer_si_l` | 160 | 96 | 125 | 4 | 720 | 已提供正式模板 |

规划投放节点：科考前哨、样本交接站。材料与加工费采用 v2 实体物品设计，具体投放状态见各型号页。

[统一实体配方与实际规划节点](<../../../08_货柜制造台/制造配方与投放总表.md>)：系列材料、加工费和门槛以当前型号页为准。
