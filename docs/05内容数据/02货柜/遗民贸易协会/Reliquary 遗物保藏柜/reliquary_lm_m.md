# REX Reliquary 遗物保藏柜 M 型

**G2 模板已接入。可制造。**

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:rex/reliquary_lm_m` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 85 组 |
| 定义空重 | 80 Kpg |
| 调度点 | 2 |
| 标签 | series.rex.reliquary |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=2` |
| 缓冲衬垫 | `level=3`，`velocity_change_bonus=8` |
| 朝向保持 | `level=1` |
| 真空隔层 | `level=2`，`exchange_time_seconds=480` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`reliquary_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/rex/reliquary_g2/rex_reliquary_g2_m` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/rex/reliquary/reliquary_m.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/rex/reliquary_g2/rex_reliquary_g2_m.nbt` |
| 规格 | M |
| 稳定货柜定义 ID | `cargoverse:rex/reliquary_lm_m`（保留） |

结构尺寸（X×Y×Z）为 8×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 200 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、create:cogwheel × 2、minecraft:white_wool × 4 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/reliquary_lm_m.json>)。


## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
