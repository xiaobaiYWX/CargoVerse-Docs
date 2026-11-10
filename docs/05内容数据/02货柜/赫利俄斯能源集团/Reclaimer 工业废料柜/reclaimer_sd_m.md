# HEC Reclaimer 工业废料柜 M 型

> **当前状态：暂不开放，制造关闭。模板：已有本系列模板，引用待调整。**
> 制作安排：关闭记录；不下达补建任务。更新：2026-11-09。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/reclaimer_sd_m` |
| 介质 | solid |
| 规格 | M |
| 容量 | 0 组 |
| 定义空重 | 64 Kpg |
| 调度点 | 2 |

## 当前配置

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reclaimer_sd_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reclaimer 工业废料柜 M 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。 本期未开放该内容形态。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "empty_mass": 64,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hec.reclaimer",
    "not_manufacturable",
    "deferred_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 0,
  "abilities": {}
}
```

[系列目录](<README.md>) · [制造商目录](<../README.md>)
