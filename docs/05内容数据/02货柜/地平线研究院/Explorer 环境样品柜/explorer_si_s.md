# HRI Explorer 环境样品柜 S 型

## 货柜介绍

Explorer为研究院样品调节温压并遮光。运单常把保存条件写得很细，项目名称却只有编号；有时接收它的研究员也没有权限知道更多。适合一支小型调查队的采样行程。标签上最常见的备注是“用途待定，请勿丢弃”。

## 型号资料

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:hri/explorer_si_s` |
| 规格 | S |
| 介质 | solid |
| 容量 | 2048 件 |
| 定义空重 | 26 Kpg |
| 调度点 | 1 |

容量按单件计数，堆叠数决定装卸步长。装满时，每件 0.1 Kpg 的货物共重 204.8 Kpg。实际空重取定义值与结构质量的较大值。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 气压调节 | `cargoverse:pressure_control` | level=1 |
| 主动调温 | `cargoverse:thermal_control` | level=1 |
| 遮光结构 | `cargoverse:light_blocking` | level=1，reduction=15 |

## G2新版结构模板

**新系列代号：`explorer_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hri/explorer_g2/hri_explorer_g2_s` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/gri/explorer/explorer_s.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hri/explorer_g2/hri_explorer_g2_s.nbt` |
| 规格 | S |
| 稳定货柜定义 ID | `cargoverse:hri/explorer_si_s`（保留） |

结构尺寸（X×Y×Z）为 4×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_s.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/hri/explorer_si_s.json>) · [系列目录](README.md)

## 现行制造材料

三层材料已于2026-11-26写入运行配方。制造按单件消耗，不按组；各规格按S基准×1／2／4／8／16。

| 层次 | 材料 | 件数 | 作用 |
| --- | --- | --- | --- |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 32 | 主体壳体与骨架 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 8 | 连接、安装与结构支承 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 4 | 连接、安装与结构支承 |
| 特殊材料 | 调温机组（`cargoverse:thermal_control_unit`） | 1 | 专项保护组件 |
| 特殊材料 | 稳压组件（`cargoverse:pressure_regulator`） | 1 | 专项保护组件 |

主体材料由介质确定，不因保护能力改换。基础封闭壳体提供的围护、防雨和遮光不重复收费。

许可、声望、蓝图费沿用当前配方。基础权益型按实际尺寸与能力使用同样用料，不用廉价配方制造同能力成品。制造商差异通过已提供能力和实际组件体现，不添加无功能的品牌材料。

[现行材料规则](<../../../03贸易点/蓝图投放/制造配方与投放总表.md>) · [产业物资与生产路线](<../../../01运输物品/04_产业物资.md>)
