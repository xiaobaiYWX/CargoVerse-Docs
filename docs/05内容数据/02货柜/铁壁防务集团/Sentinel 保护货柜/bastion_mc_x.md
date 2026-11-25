# BDS Sentinel 保护货柜 X 型

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:bds/bastion_mc_x` |
| 规格 | X |
| 介质 | solid |
| 容量 | 32768 件 |
| 定义空重 | 255 Kpg |
| 调度点 | 6 |

容量按单件计数，堆叠数决定装卸步长。装满时，每件 0.1 Kpg 的货物共重 3276.8 Kpg。实际空重取定义值与结构质量的较大值。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 缓冲衬垫 | `cargoverse:cushioning` | level=2，velocity_change_bonus=5 |
| 朝向保持 | `cargoverse:orientation_control` | level=1 |
| 遮光结构 | `cargoverse:light_blocking` | level=1，reduction=15 |

## G2新版结构模板

**新系列代号：`sentinel_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/bds/sentinel_g2/bds_sentinel_g2_x` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/bds/sentinel/sentinel_x.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/bds/sentinel_g2/bds_sentinel_g2_x.nbt` |
| 规格 | X |
| 稳定货柜定义 ID | `cargoverse:bds/bastion_mc_x`（保留） |

结构尺寸（X×Y×Z）为 12×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/bastion_mc_x.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/bds/bastion_mc_x.json>) · [系列目录](README.md)
