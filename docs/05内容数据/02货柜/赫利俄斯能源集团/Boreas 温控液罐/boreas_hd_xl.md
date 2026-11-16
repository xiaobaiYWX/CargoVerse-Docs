# HEC Boreas 温控液罐 XL 型

**G2 模板已接入。可制造。**

## 定位与承载

温敏流体大宗运输，保留密封2、隔热480秒、双向调温−20～80TU及遮光15。X／XL提高单柜容量及每调度点运量，保护能力不随规格自动升级。

| 项目 | 当前定义 |
| --- | --- |
| 资源 ID | `cargoverse:hec/boreas_hd_xl` |
| 规格／许可 | XL／XL |
| 介质 | liquid |
| 容量 | 800 桶 |
| 定义空重 | 580 Kpg |
| 调度点 | 8 |
| 每调度点容量 | 100.00 桶 |

实际空重受结构质量下限约束，实际空重需装配后测量。容量不是质量。

## G2新版结构模板

**新系列代号：`boreas_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hec/boreas_g2/hec_boreas_g2_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/hec/boreas/boreas_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hec/boreas_g2/hec_boreas_g2_xl.nbt` |
| 规格 | XL |
| 稳定货柜定义 ID | `cargoverse:hec/boreas_hd_xl`（保留） |

结构尺寸（X×Y×Z）为 24×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 保护能力

沿用本系列L型全部能力参数，完整字段见下方现行定义。大柜不提高调温、调压速率，不提供未声明的防护。

## 制造配方与投放

| 项目 | 数值／安排 |
| --- | --- |
| 蓝图打印费 | 1400 VB |
| 理想制造时间 | 70 秒（1400 tick） |
| 实体材料 | minecraft:iron_ingot × 224、minecraft:oak_planks × 112、minecraft:glass × 56、minecraft:redstone × 28、minecraft:blue_ice × 14、create:fluid_tank × 14 |
| 拟投放 | fuel_depot；X最低繁荣3、XL最低繁荣4 |
| 当前投放 | A／B 测试贸易点 |

配方按同系列L型成本的X两倍、XL三点五倍起步；实际材料、许可与费用均已落入独立配方。A／B 测试目录已开放此配方。

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/boreas_hd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/hec/boreas_hd_xl.json>)


[系列目录](README.md) · [制造商目录](../README.md)
