# VBS Aquarium 加强缓冲生物舱 XL 型

**G2 模板已接入。可制造。**

## 定位与承载

敏感生物加强缓冲运输；以BioPod同档75%舱位和较高空重换取缓冲+5。X／XL提高单柜容量及每调度点运量，保护能力不随规格自动升级。

| 项目 | 当前定义 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/aquarium_sd_xl` |
| 规格／许可 | XL／XL |
| 介质 | living |
| 容量 | 168 舱位 |
| 定义空重 | 108 Kpg |
| 调度点 | 8 |
| 每调度点容量 | 21.00 舱位 |

实际空重受结构质量下限约束，实际空重需装配后测量。容量不是质量。

## G2新版结构模板

**新系列代号：`aquarium_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/aquarium_g2/vbs_aquarium_g2_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/aquarium/aquarium_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/aquarium_g2/vbs_aquarium_g2_xl.nbt` |
| 规格 | XL |
| 稳定货柜定义 ID | `cargoverse:vbs/aquarium_sd_xl`（保留） |

结构尺寸（X×Y×Z）为 24×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 生物数据边界

单只原生数据预算仍为65536字节，整柜仍为1048576字节；不随X／XL舱位自动提高。可装数量同时受物种舱位和原生数据字节限制，复杂NBT个体可能先达到数据上限。满柜只数不能由舱位数直接推定，也不区分陆生与水生柜。

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

## 制造配方与投放

| 项目 | 数值／安排 |
| --- | --- |
| 蓝图打印费 | 2940 VB |
| 理想制造时间 | 70 秒（1400 tick） |
| 实体材料 | minecraft:iron_ingot × 224、minecraft:glass × 112、minecraft:blue_ice × 14、create:fluid_pipe × 28、create:fluid_tank × 14、minecraft:white_wool × 28 |
| 拟投放 | biosystems_station（建议，尚未投放）；X最低繁荣3、XL最低繁荣4 |
| 当前投放 | A／B 测试贸易点 |

配方按同系列L型成本的X两倍、XL三点五倍起步；实际材料、许可与费用均已落入独立配方。A／B 测试目录已开放此配方。

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_xl.json>)


[系列目录](README.md) · [制造商目录](../README.md)
