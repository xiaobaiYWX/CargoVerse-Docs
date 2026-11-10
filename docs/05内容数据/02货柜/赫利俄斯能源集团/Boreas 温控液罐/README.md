# HEC Boreas 温控液罐

正式产品线。核对：2026-11-09。**本系列已规划规格均有指定模板，无缺失。**

按 2026-11-09 明确指定的资产分配：Boreas 使用历史 Apollo SD 的 S／M／L 模板；Apollo 使用 Reactor HD 的 M／L／X 模板。保留 NBT 原文件名和既有定义 ID，这两组映射属于已确认绑定，不再列为模板缺失或引用错误。

## 产品定位

温敏工业液体运输，密封2、隔热480秒、主动调温 −20～80 TU、速率0.6 TU/s、遮光15；不提供主动稳压。

## 正式规格与模板

| 规格 | 定义 | 指定模板 | 状态 |
| --- | --- | --- | --- |
| S | [HEC Boreas 温控液罐 S 型](<boreas_hd_s.md>) | `cargoverse:cargo/hec/apollo/hec_apollo_sd_s` | 已绑定，无缺失 |
| M | [HEC Boreas 温控液罐 M 型](<boreas_hd_m.md>) | `cargoverse:cargo/hec/apollo/hec_apollo_sd_m` | 已绑定，无缺失 |
| L | [HEC Boreas 温控液罐 L 型](<boreas_hd_l.md>) | `cargoverse:cargo/hec/apollo/hec_apollo_sd_l` | 已绑定，无缺失 |

Boreas 保留 `boreas_hd_*` 定义 ID；实际模板接口为 SD，不由历史 ID 后缀推断接口。S／M／L 容量分别为 60／120／240 桶，定义空重为 45／90／190 Kpg。

未列出的规格尚未规划，不计缺失。

[制造商产品线](../README.md) · [正式目录](../../README.md)

## 状态与制作安排

同一系列的可用、待验证、待模板及关闭型号均在本页维护。型号是否能制造以工程标签为准。

| 定义 | 规格 | 当前状态 | 模板状态 | 制作安排 |
| --- | --- | --- | --- | --- |
| [cargoverse:hec/boreas_hd_l](<boreas_hd_l.md>) | L | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hec/boreas_hd_m](<boreas_hd_m.md>) | M | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hec/boreas_hd_s](<boreas_hd_s.md>) | S | 已配置，可制造 | 已绑定指定模板 | 装配、对接与满载运输待实机验证 |
