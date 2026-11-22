# REX Salvage 修复货柜 S 型

**G2 模板已接入。可制造。**

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:rex/salvage_lm_s` |
| 介质 | solid |
| 尺寸 | S |
| 容量 | 45 组 |
| 定义空重 | 30 Kpg |
| 调度点 | 1 |
| 标签 | series.rex.salvage |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 遮光结构 | `level=1`，`reduction=15` |

装载时冻结运输条件和货柜能力。各能力的适用条件和参数见[货柜能力](<../../../../04数据规范/货柜/能力/README.md>)。

## G2新版结构模板

**新系列代号：`salvage_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/rex/salvage_g2/rex_salvage_g2_s` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/rex/salvage/salvage_s.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/rex/salvage_g2/rex_salvage_g2_s.nbt` |
| 规格 | S |
| 稳定货柜定义 ID | `cargoverse:rex/salvage_lm_s`（保留） |

结构尺寸（X×Y×Z）为 4×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [heritage_gallery](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/heritage_gallery.json>) | S | 0 | 80 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:oak_planks × 8、minecraft:leather × 4、minecraft:white_wool × 2 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 80 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:oak_planks × 8、minecraft:leather × 4、minecraft:white_wool × 2 |
| [far_reach_exchange](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/far_reach_exchange.json>) | S | 0 | 80 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:oak_planks × 8、minecraft:leather × 4、minecraft:white_wool × 2 |
| [remnant_exchange](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/remnant_exchange.json>) | S | 0 | 80 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:oak_planks × 8、minecraft:leather × 4、minecraft:white_wool × 2 |


## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_s.json>)。


## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
