# HEC Boreas 温控液罐 XL 型

## 货柜介绍

Boreas用于需要照看温度的工业液体。密封罐体之外，调温、隔热与遮光共同构成它的工作边界，赫利俄斯将其写成了逐项交接的操作规程。面向大宗温敏液体的干线交付。签收时的短短一行字，背后是整条航线反复核对的同一组条件。

## 型号资料

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:hec/boreas_hd_xl` |
| 规格 | XL |
| 介质 | liquid |
| 容量 | 1024 桶 |
| 定义空重 | 580 Kpg |
| 调度点 | 8 |

液体按桶、生物按舱位计量。生物只数受物种占用舱位与原生数据预算约束。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 密封 | `cargoverse:sealing` | level=1 |
| 主动调温 | `cargoverse:thermal_control` | level=1 |
| 真空隔层 | `cargoverse:vacuum_insulation` | level=1 |
| 遮光结构 | `cargoverse:light_blocking` | level=1，reduction=15 |

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


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/boreas_hd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/hec/boreas_hd_xl.json>) · [系列目录](README.md)

## 现行制造材料

三层材料已于2026-11-26写入运行配方。制造按单件消耗，不按组；各规格按S基准×1／2／4／8／16。

| 层次 | 材料 | 件数 | 作用 |
| --- | --- | --- | --- |
| 主材料 | 铜锭（`minecraft:copper_ingot`） | 512 | 主体壳体与骨架 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 128 | 连接、安装与结构支承 |
| 辅材料 | 密封接头组（`cargoverse:sealing_joints`） | 64 | 罐体管口、密闭连接 |
| 特殊材料 | 调温机组（`cargoverse:thermal_control_unit`） | 16 | 专项保护组件 |
| 特殊材料 | 高纯陶瓷粉（`cargoverse:high_purity_ceramic_powder`） | 32 | 专项保护组件 |

主体材料由介质确定，不因保护能力改换。基础封闭壳体提供的围护、防雨和遮光不重复收费。

许可、声望、蓝图费沿用当前配方。基础权益型按实际尺寸与能力使用同样用料，不用廉价配方制造同能力成品。制造商差异通过已提供能力和实际组件体现，不添加无功能的品牌材料。

[现行材料规则](<../../../03贸易点/蓝图投放/制造配方与投放总表.md>) · [产业物资与生产路线](<../../../01运输物品/04_产业物资.md>)
