# VBS Harvest 保鲜货柜 S 型

> 正式型号；**同系列同规格／已绑定**。 核对：2026-11-06。

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/harvest_lm_s` |
| 介质 | solid |
| 尺寸 | S |
| 容量 | 60 组 |
| 定义空重 | 26 Kpg |
| 调度点 | 1 |
| 标签 | series.vbs.harvest |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=1`，`target_min=2`，`target_max=40`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板

| 核验项 | 结果 |
| --- | --- |
| 当前定义的设计系列 | `series.vbs.harvest` |
| 当前运行引用 | `cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s` |
| NBT 命名的真实归属 | VBS / harvest / LM / S |
| 系列及规格是否匹配 | 是 |
| 同系列同规格 NBT | [cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/harvest/vbs_harvest_lm_s.nbt>) |
| 制作安排 | 不需补建此规格；已绑定 |

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

本轮未改 JSON 或 NBT。旧系列模板仍属于其文件名中的系列，不视为本系列资产。

[本系列正式规格](<README.md>)

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 100 | minecraft:iron_ingot × 8、minecraft:oak_planks × 12、minecraft:white_wool × 4、minecraft:glass × 4、minecraft:blue_ice × 1 |
| [aquaculture_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/aquaculture_station.json>) | S | 0 | 100 | minecraft:iron_ingot × 8、minecraft:oak_planks × 12、minecraft:white_wool × 4、minecraft:glass × 4、minecraft:blue_ice × 1 |
| [terrace_farm](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/terrace_farm.json>) | S | 0 | 100 | minecraft:iron_ingot × 8、minecraft:oak_planks × 12、minecraft:white_wool × 4、minecraft:glass × 4、minecraft:blue_ice × 1 |

## 基础运输权益
本型号对应[制造商初始基础货柜权益](<../../基础型号/oasis_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 1 点，不修改型号定义。

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/harvest_lm_s.json>)。以下摘录省略旧 description 文案；产品定位以本页为准，运行字段保持工程现状。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 保鲜货柜 S 型",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 60,
  "empty_mass": 26,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.vbs.harvest"
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

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
