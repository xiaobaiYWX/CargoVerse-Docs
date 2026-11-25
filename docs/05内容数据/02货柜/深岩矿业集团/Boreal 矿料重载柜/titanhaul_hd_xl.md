# DMC Boreal 矿料重载柜 XL 型

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:dmc/titanhaul_hd_xl` |
| 规格 | XL |
| 介质 | solid |
| 容量 | 131072 件 |
| 定义空重 | 430 Kpg |
| 调度点 | 8 |

容量按单件计数，堆叠数决定装卸步长。装满时，每件 0.1 Kpg 的货物共重 13107.2 Kpg。实际空重取定义值与结构质量的较大值。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 围护 | `cargoverse:containment` | level=1 |
| 缓冲衬垫 | `cargoverse:cushioning` | level=1，velocity_change_bonus=2 |

## G2新版结构模板

**新系列代号：`boreal_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/dmc/boreal_g2/dmc_boreal_g2_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/dmc/boreal/boreal_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/dmc/boreal_g2/dmc_boreal_g2_xl.nbt` |
| 规格 | XL |
| 稳定货柜定义 ID | `cargoverse:dmc/titanhaul_hd_xl`（保留） |

结构尺寸（X×Y×Z）为 24×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/titanhaul_hd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/dmc/titanhaul_hd_xl.json>) · [系列目录](README.md)
