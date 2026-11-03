# HRI Crucible 样品液罐 M 型

可制造。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hri/crucible_si_m` |
| 介质 | liquid |
| 尺寸 | M |
| 容量 | 120 桶 |
| 定义空重 | 80 Kpg |
| 调度点 | 2 |
| 标签 | series.hri.crucible |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 密封 | `level=2` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=2`，`target_min=0`，`target_max=60`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 压力调节 | `level=1`，`target_min=0.5`，`target_max=1.5`，`rate_per_second=0.02`，`supported_modes=["pressurizing", "depressurizing"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:hri/crucible_si_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_m.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_m` |
| 当前 NBT | [Atlas M 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_m.nbt>)；包络 9×4×6，体积 216；标准对接接口×4 |
| 专用路径建议 | `cargoverse:cargo/hri/crucible/hri_crucible_si_m`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**无本型号原专用 NBT。** 当前能引用 Atlas 只表示占位可加载，不能当作粉料柜／封存柜／罐体等职责已经在模型中完成。

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 220 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_pipe × 2、create:fluid_tank × 2 |
| [phase_station](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/sky_station/phase_station.json>) | M | 1 | 220 | minecraft:iron_ingot × 32、minecraft:oak_planks × 16、minecraft:glass × 8、minecraft:redstone × 4、minecraft:blue_ice × 2、create:fluid_pipe × 2、create:fluid_tank × 2 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_m.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hri",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "display_name": "HRI Crucible 样品液罐 M 型",
  "description": "液体运输罐柜；容量按1000mB为一个单位，实际载荷与保护由数据包定义。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 80,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hri.crucible"
  ],
  "capacity": 120,
  "abilities": {
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
