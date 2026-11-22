# VBS Aquarium 加强缓冲生物舱 L 型

**G2 模板已接入。可制造。**

## G2新版结构模板

**新系列代号：`aquarium_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/aquarium_g2/vbs_aquarium_g2_l` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/aquarium/aquarium_l.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/aquarium_g2/vbs_aquarium_g2_l.nbt` |
| 规格 | L |
| 稳定货柜定义 ID | `cargoverse:vbs/aquarium_sd_l`（保留） |

结构尺寸（X×Y×Z）为 12×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)



## 定位与承载

加强缓冲生物舱，适用于所有已准入物种，以较少舱位与较高空重换取更强冲击保护。

| 项目 | 配置 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/aquarium_sd_l` |
| 系列／规格 | aquarium／L |
| 运输介质 | living，全部已准入物种 |
| 总舱位 | 48 |
| 配置空重 | 36 Kpg |
| 调度点 | 4 |
| 单体／整柜原生数据预算 | 65536／1048576 字节 |

装载数量取总舱位除以单只舱位的整数部分。一柜一种 EntityType，生命、名称和变种等状态随个体保存。鳕鱼和鸡都按各自物种舱位装载，牛、远古守卫者等大体型物种消耗更多舱位。实际空重取配置与结构物理质量的较大值，结构质量仍须核定。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 密封 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 真空隔层 | `level=1` |
| 主动调温 | `level=1` |
| 气压调节 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |

装载时冻结货柜能力。各能力对应的适用条件和参数见[货柜能力](<../../../../04数据规范/货柜/能力/README.md>)。

## 制造与结构

[制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_l.json>) 按实际物品和蓝图费用配置。A／B 测试目录已开放此配方。

Aquarium 搭建重点为独立减振舱框、缓冲底座、观察窗和可维护环境设备，采用 VBS 生态设备风格与标准接口。外观可表现密闭观察舱，同系列 M／L 各自导出。

## 当前定义

[工程 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_l.json>)


[系列目录](<README.md>) · [制造商目录](<../README.md>)

[系列目录](<README.md>) · [制造商目录](<../README.md>)
