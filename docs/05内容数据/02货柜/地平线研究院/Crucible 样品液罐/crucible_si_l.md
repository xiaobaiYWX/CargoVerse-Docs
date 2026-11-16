# HRI Crucible 样品液罐 L 型

**G2 模板已接入。可制造。**

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目    | 当前值                            |
| ----- | ------------------------------ |
| 资源 ID | `cargoverse:hri/crucible_si_l` |
| 介质    | liquid                         |
| 尺寸    | L                              |
| 容量    | 240 桶                          |
| 定义空重  | 170 Kpg                        |
| 调度点   | 4                              |
| 标签    | series.hri.crucible            |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 密封 | `level=2` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=2`，`target_min=0`，`target_max=60`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 压力调节 | `level=1`，`target_min=0.5`，`target_max=1.5`，`rate_per_second=0.02`，`supported_modes=["pressurizing", "depressurizing"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`crucible_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hri/crucible_g2/hri_crucible_g2_l` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/gri/crucible/crucible_l.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hri/crucible_g2/hri_crucible_g2_l.nbt` |
| 规格 | L |
| 稳定货柜定义 ID | `cargoverse:hri/crucible_si_l`（保留） |

结构尺寸（X×Y×Z）为 12×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | L | 2 | 440 | minecraft:iron_ingot × 64、minecraft:oak_planks × 32、minecraft:glass × 16、minecraft:redstone × 8、minecraft:blue_ice × 4、create:fluid_pipe × 4、create:fluid_tank × 4 |
| [phase_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/phase_station.json>) | L | 2 | 440 | minecraft:iron_ingot × 64、minecraft:oak_planks × 32、minecraft:glass × 16、minecraft:redstone × 8、minecraft:blue_ice × 4、create:fluid_pipe × 4、create:fluid_tank × 4 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_l.json>)。


## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
