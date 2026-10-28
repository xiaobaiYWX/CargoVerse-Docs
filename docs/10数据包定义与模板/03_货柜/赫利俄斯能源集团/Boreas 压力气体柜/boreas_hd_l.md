# HEC Boreas 压力气体柜 L 型

当前已接入统一液体载荷、Create 原生仓储、公共确认装卸及免费管理装卸；全型号测试站可制造。专用结构与正式产品平衡仍待完成。

| 项目 | 当前值 |
| --- | --- |
| 定义 ID | `cargoverse:hec/boreas_hd_l` |
| 介质 | 仅 liquid（包括标准 Fluid 气体） |
| 定义容量 | 240 份，每份 1000mB |
| 原生容量 | 240000mB |
| 空重 | 190Kpg；实际结构基线构成下限 |
| 普通调度点 | 4 |
| 保护能力 | 气密 2 |
| 模板 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l`（占位） |

当前数值与资源以[运行 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/boreas_hd_l.json>)为准；型号只提供定义中明确声明的能力，容量按固定原生量计算。运作规则和岩浆燃气测试见[液体运输](../../../../01货柜系统/01核心系统/13_液体运输.md)。

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hec",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "display_name": "HEC Boreas 压力气体柜 L 型",
  "description": "气密流体运输柜，适用于易挥发液体及气体；暂用同规格 AUI 标准干柜结构。",
  "size_class": "L",
  "dispatch_points": 4,
  "empty_mass": 190,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hec.boreas"
  ],
  "capacity": 240,
  "abilities": {
    "cargoverse:sealing": {
      "level": 2
    }
  }
}
```

[系列](README.md) · [制造商](../README.md)
