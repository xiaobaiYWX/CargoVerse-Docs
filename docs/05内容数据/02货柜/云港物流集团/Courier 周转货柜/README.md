# SPL Courier 周转货柜

**正式产品线。核对：2026-11-06。**

**本系列缺失规格：L。** 有同系列 NBT 但引用错误：S、M。

## 产品定位

低空重普通运输，初始型号。主要取舍：无缓冲和密封。

## 正式规格与模板

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

| 规格 | 正式型号 | 模板结论 | 当前引用的实际归属 | 同系列同规格 NBT／待制作路径 |
| --- | --- | --- | --- | --- |
| S | [SPL Courier 周转货柜 S 型](<courier_mc_s.md>) | **同系列同规格 NBT 已有／引用错误** | SPL / cargo / MC / S | `cargoverse:cargo/spl/courier/spl_courier_mc_s` |
| M | [SPL Courier 周转货柜 M 型](<courier_mc_m.md>) | **同系列同规格 NBT 已有／引用错误** | SPL / cargo / MC / M | `cargoverse:cargo/spl/courier/spl_courier_mc_m` |
| L | [SPL Courier 周转货柜 L 型](<cargo_mc_l.md>) | **同系列规格模板缺失／待制作** | SPL / cargo / MC / L | `cargoverse:cargo/spl/courier/spl_courier_mc_l` |
| X | 未规划正式型号 | 不列入缺失任务 | — | — |
| XL | 未规划正式型号 | 不列入缺失任务 | — | — |

已存在的同系列文件仍需核对接口与实际尺寸；不能把旧引用的接口当作新系列的接口。待制作路径沿当前定义的接口代号列出，仅作制作目标，本轮未改运行引用。

## 本系列现有 NBT

| 文件／资源 ID | 接口 | 规格 | 当前引用情况 |
| --- | --- | --- | --- |
| [cargoverse:cargo/spl/courier/spl_courier_mc_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/courier/spl_courier_mc_m.nbt>) | MC | M | **未被任何定义引用** |
| [cargoverse:cargo/spl/courier/spl_courier_mc_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/courier/spl_courier_mc_s.nbt>) | MC | S | **未被任何定义引用** |

## 同系列基础变体

`cargoverse:spl/starter_courier_mc_s`，实际 S 型：**同系列同规格 NBT 已有／引用错误**。当前模板 `cargoverse:cargo/spl/cargo/spl_cargo_mc_s`；同系列目标 `cargoverse:cargo/spl/courier/spl_courier_mc_s`。基础变体不增加系列或缺失规格计数。

本系列全部定义及未完成工作见下方状态表；关闭记录不属于当前制作任务。

[制造商产品线](../README.md) · [正式目录](../../README.md)

## 状态与制作安排

同一系列的可用、待验证、待模板及关闭型号均在本页维护。型号是否能制造以工程标签为准。

| 定义 | 规格 | 当前状态 | 模板状态 | 制作安排 |
| --- | --- | --- | --- | --- |
| [cargoverse:spl/cargo_mc_l](<cargo_mc_l.md>) | L | 已配置，可制造 | 缺本系列模板 | 按本型号页面补建或纠正引用 |
| [cargoverse:spl/cargo_mc_m](<cargo_mc_m.md>) | M | 暂不开放，制造关闭 | 已有本系列模板，引用待调整 | 关闭记录；不下达补建任务 |
| [cargoverse:spl/courier_mc_m](<courier_mc_m.md>) | M | 已配置，可制造 | 已有本系列模板，引用待调整 | 按本型号页面补建或纠正引用 |
| [cargoverse:spl/courier_mc_s](<courier_mc_s.md>) | S | 已配置，可制造 | 已有本系列模板，引用待调整 | 按本型号页面补建或纠正引用 |
| [cargoverse:spl/starter_courier_mc_s](<../../基础型号/spl_basic.md>) | S | 基础型，可制造 | 已有本系列模板，引用待调整 | 按本型号页面补建或纠正引用 |

旧 cargo_mc_m 定义继续关闭；当前生产使用 courier_mc 系列定义。
