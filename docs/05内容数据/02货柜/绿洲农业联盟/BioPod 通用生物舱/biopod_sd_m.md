# VBS BioPod 通用生物舱 M 型

## 货柜介绍

BioPod用调温、稳压与基础缓冲照看VBS的生物货运。克隆培养站让出货名单迅速变长，饲养员也逐渐改用批次号区分那些过于相像的乘客。常见于农场间的种群交换。每一份交接记录都要注明去处，不能只写“已卸货”。

## 型号资料

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:vbs/biopod_sd_m` |
| 规格 | M |
| 介质 | living |
| 容量 | 32 舱位 |
| 定义空重 | 14 Kpg |
| 调度点 | 2 |

液体按桶、生物按舱位计量。生物只数受物种占用舱位与原生数据预算约束。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 密封 | `cargoverse:sealing` | level=1 |
| 缓冲衬垫 | `cargoverse:cushioning` | level=1，velocity_change_bonus=2 |
| 主动调温 | `cargoverse:thermal_control` | level=1 |
| 真空隔层 | `cargoverse:vacuum_insulation` | level=1 |
| 气压调节 | `cargoverse:pressure_control` | level=1 |
| 遮光结构 | `cargoverse:light_blocking` | level=1，reduction=15 |

## G2新版结构模板

**新系列代号：`biopod_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/biopod_g2/vbs_biopod_g2_m` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/vbs/biopod/biopod_m.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/biopod_g2/vbs_biopod_g2_m.nbt` |
| 规格 | M |
| 稳定货柜定义 ID | `cargoverse:vbs/biopod_sd_m`（保留） |

结构尺寸（X×Y×Z）为 8×5×5 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)



## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_m.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/biopod_sd_m.json>) · [系列目录](README.md)

## 现行制造材料

三层材料已于2026-11-26写入运行配方。制造按单件消耗，不按组；各规格按S基准×1／2／4／8／16。

| 层次 | 材料 | 件数 | 作用 |
| --- | --- | --- | --- |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 64 | 主体壳体与骨架 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 16 | 连接、安装与结构支承 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 8 | 连接、安装与结构支承 |
| 特殊材料 | 生命维持组件（`cargoverse:life_support_module`） | 4 | 集成温控、稳压、隔热、密封及基础缓冲 |

主体材料由介质确定，不因保护能力改换。基础封闭壳体提供的围护、防雨和遮光不重复收费。生命维持组件作为集成能力包，已覆盖温控、稳压、隔热、密封与一级缓冲，不再重复叠加同用途组件。

许可、声望、蓝图费沿用当前配方。基础权益型按实际尺寸与能力使用同样用料，不用廉价配方制造同能力成品。制造商差异通过已提供能力和实际组件体现，不添加无功能的品牌材料。

[现行材料规则](<../../../03贸易点/蓝图投放/制造配方与投放总表.md>) · [产业物资与生产路线](<../../../01运输物品/04_产业物资.md>)
