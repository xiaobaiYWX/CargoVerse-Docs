# VBS Harvest 保鲜货柜 S 型（基础型）

> **当前状态：基础型，可制造。模板：本系列模板已绑定。**
> 制作安排：装配、对接与满载运输待实机验证。更新：2026-11-09。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/starter_harvest_lm_s` |
| 介质 | solid |
| 规格 | S |
| 容量 | 60 组 |
| 定义空重 | 26 Kpg |
| 调度点 | 0 |

## 当前配置

[工程定义](<../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/starter_harvest_lm_s.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 保鲜货柜 S 型（基础型）",
  "description": "基础货柜：每名玩家同时只能拥有一个，不占调度点。实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 0,
  "capacity": 60,
  "empty_mass": 26,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.vbs.harvest",
    "starter"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:vacuum_insulation": {
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 1,
      "target_min": 2,
      "target_max": 40,
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
