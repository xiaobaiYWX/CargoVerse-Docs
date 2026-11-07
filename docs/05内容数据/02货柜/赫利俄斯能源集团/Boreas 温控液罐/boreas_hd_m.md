# HEC Boreas 温控液罐 M 型

> 正式型号；**同系列规格模板缺失／待制作**。 核对：2026-11-06。

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

| 核验项 | 结果 |
| --- | --- |
| 当前定义的设计系列 | `series.hec.boreas` |
| 当前运行引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_m` |
| NBT 命名的真实归属 | AUI / atlas / SD / M |
| 系列及规格是否匹配 | **否，不能作为该型号同系列模板** |
| 同系列同规格 NBT | **没有** |
| 制作安排 | **缺失待制作：`cargoverse:cargo/hec/boreas/hec_boreas_hd_m`** |

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

本轮未改 JSON 或 NBT。旧系列模板仍属于其文件名中的系列，不视为本系列资产。

[本系列正式规格](<README.md>)

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [fuel_depot](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/fuel_depot.json>) | M | 1 | 200 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_tank × 2 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 200 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_tank × 2 |

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/boreas_hd_m.json>)。以下摘录省略旧 description 文案；产品定位以本页为准，运行字段保持工程现状。

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hec",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "display_name": "HEC Boreas 温控液罐 M 型",
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
