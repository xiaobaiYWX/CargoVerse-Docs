# HEC Boreas 温控液罐 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/boreas_hd_m` |
| 介质 | liquid |
| 尺寸 | M |
| 容量 | 120 桶 |
| 定义空重 | 90 Kpg |
| 调度点 | 2 |
| 标签 | series.hec.boreas |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 密封 | `level=2` |
| 真空隔层 | `level=2`，`exchange_time_seconds=480` |
| 主动调温 | `level=3`，`target_min=-20`，`target_max=80`，`rate_per_second=0.6`，`supported_modes=["cooling", "heating"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板

`cargoverse:cargo/aui/atlas/aui_atlas_sd_m`

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [fuel_depot](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/fuel_depot.json>) | M | 1 | 200 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_tank × 2 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 200 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_tank × 2 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/boreas_hd_m.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hec",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "display_name": "HEC Boreas 温控液罐 M 型",
  "description": "气密流体运输柜，适用于易挥发液体及气体；暂用同规格 AUI 标准干柜结构。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 90,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hec.boreas"
  ],
  "capacity": 120,
  "abilities": {
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:vacuum_insulation": {
      "level": 2,
      "exchange_time_seconds": 480
    },
    "cargoverse:thermal_control": {
      "level": 3,
      "target_min": -20,
      "target_max": 80,
      "rate_per_second": 0.6,
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
