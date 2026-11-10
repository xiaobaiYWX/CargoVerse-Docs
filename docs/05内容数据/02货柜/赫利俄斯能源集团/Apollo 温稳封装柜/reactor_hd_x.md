# HEC Apollo 温稳封装柜 X 型

> **当前状态：暂不开放，制造关闭。模板：缺本系列模板。**
> 制作安排：关闭记录；不下达补建任务。更新：2026-11-09。

兼容或预留型号，制造关闭。更新于 2026-11-03。

[系列目录](<README.md>) · [制造商目录](<../README.md>)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/reactor_hd_x` |
| 介质 | solid |
| 尺寸 | X |
| 容量 | 330 组 |
| 定义空重 | 360 Kpg |
| 调度点 | 6 |
| 标签 | series.hec.apollo、not_manufacturable |

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

## 结构模板

旧 ID `cargoverse:hec/reactor_hd_x` 当前仍指向 `cargoverse:cargo/aui/atlas/aui_atlas_sd_x`，仅保留关闭记录，不制作新模板。正在使用的 Apollo 型号为 apollo_sd_s／m／l，已明确绑定 Reactor HD-M／L／X，见[系列目录](README.md)。

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| 当前无配方 | — | — | — | — |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_x.json>)。以下为现行完整定义；关闭状态不因归入正式文档而改变。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_x",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 温稳封装柜 X 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 330,
  "empty_mass": 360,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hec.apollo",
    "not_manufacturable"
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
