# HRI Explorer 环境样品柜 M 型

> **当前状态：暂不开放，制造关闭。模板：已有本系列模板，引用待调整。**
> 制作安排：关闭记录；不下达补建任务。更新：2026-11-09。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hri/archive_si_m` |
| 介质 | solid |
| 规格 | M |
| 容量 | 85 组 |
| 定义空重 | 60 Kpg |
| 调度点 | 2 |

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/archive_si_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Explorer 环境样品柜 M 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 85,
  "empty_mass": 60,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hri.explorer",
    "not_manufacturable"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
    },
    "cargoverse:orientation_control": {
      "level": 1
    },
    "cargoverse:humidity_control": {
      "level": 1,
      "target_min": 20,
      "target_max": 60,
      "rate_per_second": 1,
      "supported_modes": [
        "dehumidifying"
      ]
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
    "cargoverse:pressure_control": {
      "level": 1,
      "target_min": 0.5,
      "target_max": 1.5,
      "rate_per_second": 0.02,
      "supported_modes": [
        "pressurizing",
        "depressurizing"
      ]
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

[系列目录](<README.md>) · [制造商目录](<../README.md>)
