# SPL Express 正放快运柜 S 型

> **当前状态：已配置，可制造。模板：本系列模板已绑定。**
> 制作安排：需制作G2新版模板；以本页G2新版结构模板章节为准。

> 正式型号；**同系列同规格／已绑定**。 核对：2026-11-06。

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:spl/express_mc_s` |
| 介质 | solid |
| 尺寸 | S |
| 容量 | 30 组 |
| 定义空重 | 14 Kpg |
| 调度点 | 1 |
| 标签 | series.spl.express |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 朝向保持 | `level=1` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`express_g2`；状态：需制作G2新版模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/spl/express_g2/spl_express_g2_mc_s` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/spl/express_g2/spl_express_g2_mc_s.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/spl/express_g2/spl_express_g2_mc_s.nbt` |
| 规格／接口代号 | S／MC |
| 当前运行模板（旧版参考） | `cargoverse:cargo/spl/express/spl_express_mc_s` |
| 稳定货柜定义 ID | `cargoverse:spl/express_mc_s`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [civic_distribution](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/civic_distribution.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |
| [longhaul_port](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/sky_station/longhaul_port.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 110 | minecraft:iron_ingot × 8、minecraft:copper_ingot × 8、minecraft:white_wool × 4、minecraft:repeater × 1、create:cogwheel × 1 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>)。以下摘录省略旧 description 文案；产品定位以本页为准，运行字段保持工程现状。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/express/spl_express_mc_s",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Express 正放快运柜 S 型",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 30,
  "empty_mass": 14,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.express"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
    },
    "cargoverse:orientation_control": {
      "level": 1
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。

[系列目录](<README.md>) · [制造商目录](<../README.md>)
