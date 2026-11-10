# AUI Vulcan 干燥工业柜

**正式产品线。核对：2026-11-06。**

**本系列缺失规格：无。** 有同系列 NBT 但引用错误：无。

## 产品定位

干燥粉料与工业裸件。主要取舍：较重、无调温。

## 正式规格与模板

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

| 规格 | 正式型号 | 模板结论 | 当前引用的实际归属 | 同系列同规格 NBT／待制作路径 |
| --- | --- | --- | --- | --- |
| S | 未规划正式型号 | 不列入缺失任务 | — | — |
| M | [AUI Vulcan 干燥工业柜 M 型](<vulcan_sd_m.md>) | **同系列同规格／已绑定** | AUI / vulcan / SD / M | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_m` |
| L | [AUI Vulcan 干燥工业柜 L 型](<vulcan_sd_l.md>) | **同系列同规格／已绑定** | AUI / vulcan / SD / L | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_l` |
| X | [AUI Vulcan 干燥工业柜 X 型](<vulcan_sd_x.md>) | **同系列同规格／已绑定** | AUI / vulcan / SD / X | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_x` |
| XL | 未规划正式型号 | 不列入缺失任务 | — | — |

已存在的同系列文件仍需核对接口与实际尺寸；不能把旧引用的接口当作新系列的接口。待制作路径沿当前定义的接口代号列出，仅作制作目标，本轮未改运行引用。

## 本系列现有 NBT

| 文件／资源 ID | 接口 | 规格 | 当前引用情况 |
| --- | --- | --- | --- |
| [cargoverse:cargo/aui/vulcan/aui_vulcan_sd_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/vulcan/aui_vulcan_sd_l.nbt>) | SD | L | `cargoverse:aui/vulcan_sd_l` |
| [cargoverse:cargo/aui/vulcan/aui_vulcan_sd_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/vulcan/aui_vulcan_sd_m.nbt>) | SD | M | `cargoverse:aui/vulcan_sd_m` |
| [cargoverse:cargo/aui/vulcan/aui_vulcan_sd_x](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/vulcan/aui_vulcan_sd_x.nbt>) | SD | X | `cargoverse:aui/vulcan_sd_x` |

本系列全部定义及未完成工作见下方状态表；关闭记录不属于当前制作任务。

[制造商产品线](../README.md) · [正式目录](../../README.md)

## 状态与制作安排

同一系列的可用、待验证、待模板及关闭型号均在本页维护。型号是否能制造以工程标签为准。

| 定义 | 规格 | 当前状态 | 模板状态 | 制作安排 |
| --- | --- | --- | --- | --- |
| [cargoverse:aui/nomad_hd_l](<nomad_hd_l.md>) | L | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:aui/nomad_hd_m](<nomad_hd_m.md>) | M | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:aui/nomad_hd_x](<nomad_hd_x.md>) | X | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:aui/vulcan_sd_l](<vulcan_sd_l.md>) | L | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |
| [cargoverse:aui/vulcan_sd_m](<vulcan_sd_m.md>) | M | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |
| [cargoverse:aui/vulcan_sd_x](<vulcan_sd_x.md>) | X | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |

旧 nomad_hd_m／l／x 定义继续关闭；当前生产使用 vulcan_sd 系列定义。
