# HEC Apollo 温稳封装柜 X 型

> **当前状态：已配置，可制造。模板：已绑定指定模板。**
> 制作安排：需制作G2新版模板；以本页G2新版结构模板章节为准。

> 正式型号；**指定旧版模板已绑定；G2待制作**。核对：2026-11-09。

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目    | 当前值                          |
| ----- | ---------------------------- |
| 资源 ID | `cargoverse:hec/apollo_sd_l` |
| 介质    | solid                        |
| 尺寸    | X                            |
| 容量    | 550 组                        |
| 定义空重  | 245 Kpg                      |
| 调度点   | 6                            |
| 标签    | series.hec.apollo            |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=2` |
| 密封 | `level=2` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=2`，`target_min=0`，`target_max=60`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`apollo_g2`；状态：需制作G2新版模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hec/apollo_g2/hec_apollo_g2_hd_x` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/hec/apollo_g2/hec_apollo_g2_hd_x.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hec/apollo_g2/hec_apollo_g2_hd_x.nbt` |
| 规格／接口代号 | X／HD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/hec/reactor/hec_reactor_hd_x` |
| 稳定货柜定义 ID | `cargoverse:hec/apollo_sd_l`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [chemical_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/chemical_works.json>) | X | 2 | 510 | minecraft:iron_ingot × 64、minecraft:copper_ingot × 32、minecraft:glass × 16、minecraft:redstone × 8、minecraft:blue_ice × 7 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | X | 2 | 510 | minecraft:iron_ingot × 64、minecraft:copper_ingot × 32、minecraft:glass × 16、minecraft:redstone × 8、minecraft:blue_ice × 7 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_l.json>)。以下为现行完整定义。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_x",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 温稳封装柜 X 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 550,
  "empty_mass": 245,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hec.apollo"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 2
    },
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:vacuum_insulation": {
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 2,
      "target_min": 0,
      "target_max": 60,
      "rate_per_second": 0.3,
      "supported_modes": [
        "cooling",
        "heating"
      ]
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
