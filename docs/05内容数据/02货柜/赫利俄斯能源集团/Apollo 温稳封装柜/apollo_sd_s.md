# HEC Apollo 温稳封装柜 M 型

> **当前状态：已配置，可制造。模板：已绑定指定模板。**
> 制作安排：装配、对接与满载运输待实机验证。更新：2026-11-09。

> 正式型号；**指定模板已绑定，无缺失**。核对：2026-11-09。

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/apollo_sd_s` |
| 介质 | solid |
| 尺寸 | M |
| 容量 | 110 组 |
| 定义空重 | 60 Kpg |
| 调度点 | 2 |
| 标签 | series.hec.apollo |

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

按 2026-11-09 明确指定的资产分配：Boreas 使用历史 Apollo SD 的 S／M／L 模板；Apollo 使用 Reactor HD 的 M／L／X 模板。保留 NBT 原文件名和既有定义 ID，这两组映射属于已确认绑定，不再列为模板缺失或引用错误。

| 核验项 | 结果 |
| --- | --- |
| 当前运行引用 | `cargoverse:cargo/hec/reactor/hec_reactor_hd_m` |
| 实际接口与规格 | HD / M |
| 模板文件 | 已存在，无需补建 |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [biosystems_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/biosystems_station.json>) | M | 0 | 130 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 8、minecraft:glass × 4、minecraft:redstone × 2、minecraft:blue_ice × 2 |
| [chemical_works](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/chemical_works.json>) | M | 0 | 130 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 8、minecraft:glass × 4、minecraft:redstone × 2、minecraft:blue_ice × 2 |
| [fuel_depot](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/fuel_depot.json>) | M | 0 | 130 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 8、minecraft:glass × 4、minecraft:redstone × 2、minecraft:blue_ice × 2 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 0 | 130 | minecraft:iron_ingot × 16、minecraft:copper_ingot × 8、minecraft:glass × 4、minecraft:redstone × 2、minecraft:blue_ice × 2 |

## 基础运输权益
本型号对应[制造商初始基础货柜权益](<../../基础型号/hec_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 2 点，不修改型号定义。

## 当前配置摘录

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/apollo_sd_s.json>)。以下为现行完整定义。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 温稳封装柜 M 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 110,
  "empty_mass": 60,
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
