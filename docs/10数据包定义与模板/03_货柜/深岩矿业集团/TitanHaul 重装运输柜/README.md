# TitanHaul 重装运输柜

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。

制造商：深岩矿业集团 / Deepcore Mining Corporation

[返回制造商](<../README.md>) · [货柜目录](<../../README.md>)

面向采矿设备、重型载具及重建材的大宗运输，以厚重结构换取高容量与稳定承载。

允许分类：原料资源（`raw_resource`）、机械设备（`machinery`）、载具与部件（`vehicle`）、建筑构件（`construction_material`）、物流与仓储（`logistics_equipment`）。分类按 2026-10-20 的十四类方案更新，未列出分类不允许。

消除的运输要求：无。设计缺陷：无。所有货物的限时要求继续生效；御寒不代表冷藏或延长保质期。

| 货柜定义 | 资源 ID | 基础容量（个） | 基础空重 Kpg | 基础耐久 | 调度点 | v2 加工费 VB | 结构状态 |
| --- | --- | --- | --- | --- | --- | --- | --- |
| [DMC TitanHaul 重装运输柜 L 型](<titanhaul_hd_l.md>) | `cargoverse:dmc/titanhaul_hd_l` | 260 | 108 | 180 | 4 | 560 | 已提供正式模板 |
| [DMC TitanHaul 重装运输柜 X 型](<titanhaul_hd_x.md>) | `cargoverse:dmc/titanhaul_hd_x` | 455 | 189 | 180 | 6 | 980 | 已提供正式模板 |
| [DMC TitanHaul 重装运输柜 XL 型](<titanhaul_hd_xl.md>) | `cargoverse:dmc/titanhaul_hd_xl` | 780 | 324 | 180 | 8 | 1680 | 已提供正式模板 |

规划投放节点：大型矿区、重工装备港。材料与加工费采用 v2 实体物品设计，具体投放状态见各型号页。

[统一实体配方与实际规划节点](<../../../08_货柜制造台/制造配方与投放总表.md>)：系列材料、加工费和门槛以当前型号页为准。
