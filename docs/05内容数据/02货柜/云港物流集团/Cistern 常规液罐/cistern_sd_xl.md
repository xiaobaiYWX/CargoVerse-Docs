# SPL Cistern 常规液罐 XL 型

2026-11-25 同步。G2 模板已接入，可制造。实际结构质量、满载起吊和航程需实测。

## 定义与承载

| 项目 | 配置 |
| --- | --- |
| 定义 ID | `cargoverse:spl/cistern_sd_xl` |
| 规格 | XL |
| 介质 | liquid |
| 容量 | 1024 桶 |
| 定义空重 | 420 Kpg |
| 调度点 | 8 |

液体按桶、生物按舱位计量。生物只数受物种占用舱位与原生数据预算约束。

## 保护能力

| 能力 | ID | 参数 |
| --- | --- | --- |
| 密封 | `cargoverse:sealing` | level=1 |

## G2新版结构模板

**新系列代号：`cistern_g2`；状态：已绑定 G2 模板。** 更新：2026-11-16。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/spl/cistern_g2/spl_cistern_g2_xl` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/g2/spl/cistern/cistern_xl.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/spl/cistern_g2/spl_cistern_g2_xl.nbt` |
| 规格 | XL |
| 稳定货柜定义 ID | `cargoverse:spl/cistern_sd_xl`（保留） |

结构尺寸（X×Y×Z）为 24×9×10 格。

已核对质量标记和标准对接口。实际空重与满载起吊待实机验证。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造与查阅

[现行定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cistern_sd_xl.json>) · [制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/spl/cistern_sd_xl.json>) · [系列目录](README.md)
