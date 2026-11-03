# VBS BioPod 陆生运输舱 S 型

可在测试站制造，装卸验证型号。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_s` |
| 介质 | living |
| 尺寸 | S |
| 容量 | 16 舱位 |
| 定义空重 | 6 Kpg |
| 调度点 | 1 |
| 标签 | series.vbs.biopod、validation_content |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=2` |
| 缓冲衬垫 | `level=1`，`velocity_change_bonus=2` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=1`，`target_min=5`，`target_max=45`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 压力调节 | `level=1`，`target_min=0.5`，`target_max=1.5`，`rate_per_second=0.02`，`supported_modes=["pressurizing", "depressurizing"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

生活环境与原生数据预算见下方当前 JSON。

## 结构模板
| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:vbs/biopod_sd_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_s.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_s` |
| 当前 NBT | [Atlas S 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_s.nbt>)；包络 7×3×5，体积 105；标准对接接口×2 |
| 专用路径建议 | `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_s`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**原自用模板候选：** `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_s` · [原 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_s.nbt>)。

只读结构检查：包络 6×4×6；标准对接接口×4；质量占位 4 个；分类占位 2 个；警示占位 10 个（槽号 0／1／2／3／4）；实体 0 个。这不是碰撞、实际质量、密封性或 Sable 连接验收。

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | S | 0 | 160 | minecraft:iron_ingot × 16、minecraft:glass × 4、minecraft:blue_ice × 1、create:fluid_pipe × 1、minecraft:white_wool × 2、minecraft:hay_block × 2 |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_s.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 陆生运输舱 S 型",
  "description": "陆生活物舱，当前使用同规格AUI占位结构；舱位与材料为首轮验证参数。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "empty_mass": 6,
  "allowed_cargo_classes": [
    "living"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.vbs.biopod",
    "validation_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 16,
  "living_chamber": {
    "environment": "land",
    "max_entity_bytes": 65536,
    "max_total_bytes": 1048576
  },
  "abilities": {
    "cargoverse:containment": {
      "level": 1
    },
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
    },
    "cargoverse:vacuum_insulation": {
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 1,
      "target_min": 5,
      "target_max": 45,
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
