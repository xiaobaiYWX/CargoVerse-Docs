# HEC Apollo 温稳封装柜

正式产品线。核对：2026-11-09。**本系列已规划规格均有指定模板，无缺失。**

按 2026-11-09 明确指定的资产分配：Boreas 使用历史 Apollo SD 的 S／M／L 模板；Apollo 使用 Reactor HD 的 M／L／X 模板。保留 NBT 原文件名和既有定义 ID，这两组映射属于已确认绑定，不再列为模板缺失或引用错误。

## 产品定位

温敏固体工业品运输，围护2、密封2、隔热240秒、主动调温0～60 TU、速率0.3 TU/s、遮光15。

## 正式规格与模板

| 规格 | 定义 | 指定模板 | 状态 |
| --- | --- | --- | --- |
| M | [HEC Apollo 温稳封装柜 M 型](<apollo_sd_s.md>) | `cargoverse:cargo/hec/reactor/hec_reactor_hd_m` | 已绑定，无缺失 |
| L | [HEC Apollo 温稳封装柜 L 型](<apollo_sd_m.md>) | `cargoverse:cargo/hec/reactor/hec_reactor_hd_l` | 已绑定，无缺失 |
| X | [HEC Apollo 温稳封装柜 X 型](<apollo_sd_l.md>) | `cargoverse:cargo/hec/reactor/hec_reactor_hd_x` | 已绑定，无缺失 |

Apollo 的旧定义 ID 后缀 s／m／l 对应实际 M／L／X；基础型 `starter_apollo_sd_s` 同样使用 Reactor HD-M。

未列出的规格尚未规划，不计缺失。

[制造商产品线](../README.md) · [正式目录](../../README.md)

## 状态与制作安排

同一系列的可用、待验证、待模板及关闭型号均在本页维护。型号是否能制造以工程标签为准。

| 定义 | 规格 | 当前状态 | 模板状态 | 制作安排 |
| --- | --- | --- | --- | --- |
| [cargoverse:hec/apollo_sd_l](<apollo_sd_l.md>) | X | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hec/apollo_sd_m](<apollo_sd_m.md>) | L | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hec/apollo_sd_s](<apollo_sd_s.md>) | M | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hec/reactor_hd_l](<reactor_hd_l.md>) | L | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:hec/reactor_hd_m](<reactor_hd_m.md>) | M | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:hec/reactor_hd_x](<reactor_hd_x.md>) | X | 暂不开放，制造关闭 | 缺本系列模板 | 关闭记录；不下达补建任务 |
| [cargoverse:hec/starter_apollo_sd_s](<../../基础型号/hec_basic.md>) | M | 基础型，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |

旧 reactor_hd_m／l／x 定义继续关闭，仅保留兼容记录。当前 Apollo 使用 apollo_sd_s／m／l 定义及 Reactor HD-M／L／X 模板，两个 ID 集合不可混淆。
