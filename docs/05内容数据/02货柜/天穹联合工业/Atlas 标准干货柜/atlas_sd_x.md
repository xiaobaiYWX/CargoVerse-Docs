# AUI Atlas 标准干货柜 X 型

## 货柜介绍

Atlas伴随AUI的飞艇与工业零件遍布航港。熟悉它的维修工常能直接报出紧固件编号，采购员也因此很难再换一套标准。为干线批量运输放大的柜体，仍沿用工人熟悉的装卸规程。AUI认为，扩建不该意味着从头学习。

## 型号资料

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:aui/atlas_sd_x` |
| 规格 | X |
| 介质 | solid |
| 容量 | 32768 件 |
| 定义空重 | 180 Kpg |
| 调度点 | 6 |

容量按单件计数，堆叠数决定装卸步长。装满时，每件 0.1 Kpg 的货物共重 3276.8 Kpg。实际空重取定义值与结构质量的较大值。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 围护 | `cargoverse:containment` | level=1 |
| 防水柜体 | `cargoverse:waterproof_body` | 启用 |
| 遮光结构 | `cargoverse:light_blocking` | level=1，reduction=15 |

## G2新版结构模板

**新系列代号：`atlas_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/aui/atlas_g2/aui_atlas_g2_x` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/aui/atlas/atlas_x.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/aui/atlas_g2/aui_atlas_g2_x.nbt` |
| 规格 | X |
| 稳定货柜定义 ID | `cargoverse:aui/atlas_sd_x`（保留） |

结构尺寸（X×Y×Z）为 12×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/atlas_sd_x.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/aui/atlas_sd_x.json>) · [系列目录](README.md)

## 现行制造材料

三层材料已于2026-11-26写入运行配方。制造按单件消耗，不按组；各规格按S基准×1／2／4／8／16。

| 层次 | 材料 | 件数 | 作用 |
| --- | --- | --- | --- |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 256 | 主体壳体与骨架 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 64 | 连接、安装与结构支承 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 32 | 连接、安装与结构支承 |

主体材料由介质确定，不因保护能力改换。基础封闭壳体提供的围护、防雨和遮光不重复收费。

许可、声望、蓝图费沿用当前配方。基础权益型按实际尺寸与能力使用同样用料，不用廉价配方制造同能力成品。制造商差异通过已提供能力和实际组件体现，不添加无功能的品牌材料。

[现行材料规则](<../../../03贸易点/蓝图投放/制造配方与投放总表.md>) · [产业物资与生产路线](<../../../01运输物品/04_产业物资.md>)
