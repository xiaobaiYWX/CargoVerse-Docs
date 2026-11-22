# HRI Explorer 环境样品柜 L 型

**G2 模板已接入。可制造。**

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hri/explorer_si_l` |
| 介质 | solid |
| 尺寸 | L |
| 容量 | 210 组 |
| 定义空重 | 125 Kpg |
| 调度点 | 4 |
| 标签 | series.hri.explorer |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 朝向保持 | `level=1` |
| 真空隔层 | `level=1` |
| 主动调温 | `level=2` |
| 气压调节 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |
| 防水柜体 | 启用 |

装载时冻结货柜能力。各能力对应的适用条件和参数见[货柜能力](<../../../../04数据规范/货柜/能力/README.md>)。

## G2新版结构模板

**新系列代号：`explorer_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hri/explorer_g2/hri_explorer_g2_l` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/gri/explorer/explorer_l.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hri/explorer_g2/hri_explorer_g2_l.nbt` |
| 规格 | L |
| 稳定货柜定义 ID | `cargoverse:hri/explorer_si_l`（保留） |

结构尺寸（X×Y×Z）为 12×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [precision_center](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/precision_center.json>) | L | 2 | 920 | minecraft:iron_ingot × 48、minecraft:glass × 32、minecraft:white_wool × 32、minecraft:redstone × 16、minecraft:sponge × 4、minecraft:blue_ice × 4、create:fluid_pipe × 4、create:cogwheel × 4 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 920 | minecraft:iron_ingot × 48、minecraft:glass × 32、minecraft:white_wool × 32、minecraft:redstone × 16、minecraft:sponge × 4、minecraft:blue_ice × 4、create:fluid_pipe × 4、create:cogwheel × 4 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_l.json>)。


## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
