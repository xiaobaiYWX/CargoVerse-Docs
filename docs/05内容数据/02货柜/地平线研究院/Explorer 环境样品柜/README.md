# HRI Explorer 环境样品柜

**正式产品线。核对：2026-11-06。**

**本系列缺失规格：无。** 有同系列 NBT 但引用错误：无。

## 产品定位

小批量多条件样品，初始型号。主要取舍：容量小，不能防粉末逸散。

## 正式规格与模板

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

| 规格 | 正式型号 | 模板结论 | 当前引用的实际归属 | 同系列同规格 NBT／待制作路径 |
| --- | --- | --- | --- | --- |
| S | [HRI Explorer 环境样品柜 S 型](<explorer_si_s.md>) | **同系列同规格／已绑定** | HRI / explorer / SI / S | `cargoverse:cargo/hri/explorer/hri_explorer_si_s` |
| M | [HRI Explorer 环境样品柜 M 型](<explorer_si_m.md>) | **同系列同规格／已绑定** | HRI / explorer / SI / M | `cargoverse:cargo/hri/explorer/hri_explorer_si_m` |
| L | [HRI Explorer 环境样品柜 L 型](<explorer_si_l.md>) | **同系列同规格／已绑定** | HRI / explorer / SI / L | `cargoverse:cargo/hri/explorer/hri_explorer_si_l` |
| X | 未规划正式型号 | 不列入缺失任务 | — | — |
| XL | 未规划正式型号 | 不列入缺失任务 | — | — |

已存在的同系列文件仍需核对接口与实际尺寸；不能把旧引用的接口当作新系列的接口。待制作路径沿当前定义的接口代号列出，仅作制作目标，本轮未改运行引用。

## 本系列现有 NBT

| 文件／资源 ID | 接口 | 规格 | 当前引用情况 |
| --- | --- | --- | --- |
| [cargoverse:cargo/hri/explorer/hri_explorer_si_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_l.nbt>) | SI | L | `cargoverse:hri/explorer_si_l` |
| [cargoverse:cargo/hri/explorer/hri_explorer_si_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_m.nbt>) | SI | M | `cargoverse:hri/explorer_si_m` |
| [cargoverse:cargo/hri/explorer/hri_explorer_si_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_s.nbt>) | SI | S | `cargoverse:hri/explorer_si_s`、`cargoverse:hri/starter_explorer_si_s` |

## 同系列基础变体

`cargoverse:hri/starter_explorer_si_s`，实际 S 型：**同系列同规格／已绑定**。当前模板 `cargoverse:cargo/hri/explorer/hri_explorer_si_s`；同系列目标 `cargoverse:cargo/hri/explorer/hri_explorer_si_s`。基础变体不增加系列或缺失规格计数。

本系列全部定义及未完成工作见下方状态表；关闭记录不属于当前制作任务。

[制造商产品线](../README.md) · [正式目录](../../README.md)

## 状态与制作安排

同一系列的可用、待验证、待模板及关闭型号均在本页维护。型号是否能制造以工程标签为准。

| 定义 | 规格 | 当前状态 | 模板状态 | 制作安排 |
| --- | --- | --- | --- | --- |
| [cargoverse:hri/archive_si_m](<archive_si_m.md>) | M | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:hri/archive_si_s](<archive_si_s.md>) | S | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:hri/explorer_si_l](<explorer_si_l.md>) | L | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hri/explorer_si_m](<explorer_si_m.md>) | M | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hri/explorer_si_s](<explorer_si_s.md>) | S | 已配置，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |
| [cargoverse:hri/starter_explorer_si_s](<../../基础型号/hri_basic.md>) | S | 基础型，可制造 | 本系列模板已绑定 | 装配、对接与满载运输待实机验证 |

旧 archive_si_s／m 定义继续关闭；当前生产使用 explorer_si 系列定义。
