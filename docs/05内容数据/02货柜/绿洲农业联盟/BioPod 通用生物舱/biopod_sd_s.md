# VBS BioPod 通用生物舱 S 型

**G2 模板已接入。可制造，待实运验证。**

## G2新版结构模板

**新系列代号：`biopod_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/biopod_g2/vbs_biopod_g2_s` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/biopod/biopod_s.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/biopod_g2/vbs_biopod_g2_s.nbt` |
| 规格 | S |
| 稳定货柜定义 ID | `cargoverse:vbs/biopod_sd_s`（保留） |

结构尺寸（X×Y×Z）为 4×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)



## 定位与承载

通用生物运输舱，提供调温、稳压、遮光与基础缓冲，适用于所有已准入物种。

| 项目 | 配置 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_s` |
| 系列／规格 | biopod／S |
| 运输介质 | living，全部已准入物种 |
| 总舱位 | 16 |
| 配置空重 | 6 Kpg |
| 调度点 | 1 |
| 单体／整柜原生数据预算 | 65536／1048576 字节 |

装载数量取总舱位除以单只舱位的整数部分。一柜一种 EntityType，生命、名称和变种等状态随个体保存。鳕鱼和鸡都按各自物种舱位装载，牛、远古守卫者等大体型物种消耗更多舱位。实际空重取配置与结构物理质量的较大值，结构质量仍须核定。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 缓冲衬垫 | `level=1`，`velocity_change_bonus=2` |
| 真空隔层 | `level=1` |
| 主动调温 | `level=1` |
| 气压调节 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |

装载时冻结货柜能力。各能力对应的适用条件和参数见[货柜能力](<../../../../04数据规范/货柜/能力/README.md>)。

## 制造与结构

[制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/biopod_sd_s.json>) 按实际物品和蓝图费用配置。现有测试目录与自然站渠道沿定义读取本型号。

BioPod 使用自身 biopod 系列 S／M／L NBT，当前定义已与对应文件一致。

## 当前定义

[工程 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_s.json>)


[系列目录](<README.md>) · [制造商目录](<../README.md>)

[系列目录](<README.md>) · [制造商目录](<../README.md>)
