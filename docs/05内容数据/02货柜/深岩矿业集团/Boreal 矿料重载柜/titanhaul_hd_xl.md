# DMC Boreal 矿料重载柜 XL 型

**G2 模板已接入。可制造。**

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:dmc/titanhaul_hd_xl` |
| 介质 | solid |
| 尺寸 | XL |
| 容量 | 1250 组 |
| 定义空重 | 430 Kpg |
| 调度点 | 8 |
| 标签 | series.dmc.boreal |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 缓冲衬垫 | `level=1`，`velocity_change_bonus=2` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`boreal_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/dmc/boreal_g2/dmc_boreal_g2_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/dmc/boreal/boreal_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/dmc/boreal_g2/dmc_boreal_g2_xl.nbt` |
| 规格 | XL |
| 稳定货柜定义 ID | `cargoverse:dmc/titanhaul_hd_xl`（保留） |

结构尺寸（X×Y×Z）为 24×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [heavy_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/heavy_works.json>) | XL | 4 | 1800 | minecraft:iron_ingot × 336、minecraft:copper_ingot × 96、minecraft:chain × 48、minecraft:piston × 12、minecraft:white_wool × 24 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | XL | 4 | 1800 | minecraft:iron_ingot × 336、minecraft:copper_ingot × 96、minecraft:chain × 48、minecraft:piston × 12、minecraft:white_wool × 24 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/titanhaul_hd_xl.json>)。


## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
