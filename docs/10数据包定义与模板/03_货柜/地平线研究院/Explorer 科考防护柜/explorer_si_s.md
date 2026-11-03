# HRI Explorer 环境样品柜 S 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hri/explorer_si_s` |
| 介质 | solid |
| 尺寸 | S |
| 容量 | 35 组 |
| 定义空重 | 26 Kpg |
| 调度点 | 1 |
| 标签 | series.hri.explorer |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=2` |
| 缓冲衬垫 | `level=2`，`velocity_change_bonus=5` |
| 朝向保持 | `level=1` |
| 湿度控制 | `level=1`，`target_min=20`，`target_max=60`，`rate_per_second=1`，`supported_modes=["dehumidifying"]` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=2`，`target_min=0`，`target_max=60`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 压力调节 | `level=1`，`target_min=0.5`，`target_max=1.5`，`rate_per_second=0.02`，`supported_modes=["pressurizing", "depressurizing"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 实际配置 |
| --- | --- |
| 定义 | [cargoverse:hri/explorer_si_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_s.json>) |
| 名称／规格 | HRI Explorer 科考防护柜 S 型／S |
| 结构 ID | `cargoverse:cargo/hri/explorer/hri_explorer_si_s` |
| NBT | [项目结构文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/explorer/hri_explorer_si_s.nbt>) |
| 包络 X×Y×Z | 7×4×5 |
| 实际接口 | 滑轨接口×1 |
| 运行标记 | 分类 2、质量 1、词条 10（0～4 齐全） |

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [precision_center](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/factory/sky_station/precision_center.json>) | S | 0 | 230 | minecraft:iron_ingot × 12、minecraft:glass × 8、minecraft:white_wool × 8、minecraft:redstone × 4、minecraft:sponge × 1、minecraft:blue_ice × 1、create:fluid_pipe × 1、create:cogwheel × 1 |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 230 | minecraft:iron_ingot × 12、minecraft:glass × 8、minecraft:white_wool × 8、minecraft:redstone × 4、minecraft:sponge × 1、minecraft:blue_ice × 1、create:fluid_pipe × 1、create:cogwheel × 1 |
| [field_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/field_station.json>) | S | 0 | 230 | minecraft:iron_ingot × 12、minecraft:glass × 8、minecraft:white_wool × 8、minecraft:redstone × 4、minecraft:sponge × 1、minecraft:blue_ice × 1、create:fluid_pipe × 1、create:cogwheel × 1 |

## 基础运输权益
本型号对应[制造商初始基础货柜权益](<../../../05_基础货柜/hri_basic.md>)。通过基础权益领取的资产免调度点；普通制造的同型号仍使用 1 点，不修改型号定义。

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/explorer_si_s.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/explorer/hri_explorer_si_s",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Explorer 环境样品柜 S 型",
  "description": "实际物品运输货柜；承载形态与运输保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 35,
  "empty_mass": 26,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hri.explorer"
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

## 实机验收

模板装配、满载起吊、对接及持续航程需在游戏中核验。当前数值以数据包配置为准。
