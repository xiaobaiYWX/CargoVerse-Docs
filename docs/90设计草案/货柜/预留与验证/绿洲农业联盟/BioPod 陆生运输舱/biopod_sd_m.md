# VBS BioPod 陆生运输舱 M 型

> **非正式内容：测试验证，非正式；不列入正式型号与制作缺失数。** 核对：2026-11-06。

可在测试站制造，装卸验证型号。更新于 2026-11-03。

[系列目录](<README.md>) · [制造商目录](<../../../../../05内容数据/02货柜/绿洲农业联盟/README.md>)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_m` |
| 介质 | living |
| 尺寸 | M |
| 容量 | 32 舱位 |
| 定义空重 | 14 Kpg |
| 调度点 | 2 |
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

| 核验项 | 结果 |
| --- | --- |
| 当前定义的设计系列 | `series.vbs.biopod` |
| 当前运行引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_m` |
| NBT 命名的真实归属 | AUI / atlas / SD / M |
| 系列及规格是否匹配 | **否，不能作为该型号同系列模板** |
| 同系列同规格 NBT | [cargoverse:cargo/vbs/biopod/vbs_biopod_sd_m](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_m.nbt>) |
| 制作安排 | 非正式内容，不下达正式模板制作任务 |

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

本轮未改 JSON 或 NBT。旧系列模板仍属于其文件名中的系列，不视为本系列资产。

[非正式内容目录](<../../README.md>)

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| [all_containers](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>) | M | 1 | 320 | minecraft:iron_ingot × 32、minecraft:glass × 8、minecraft:blue_ice × 2、create:fluid_pipe × 2、minecraft:white_wool × 4、minecraft:hay_block × 4 |

## 当前配置摘录

[工程定义](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_m.json>)。以下摘录省略旧 description 文案；产品定位以本页为准，运行字段保持工程现状。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 陆生运输舱 M 型",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "empty_mass": 14,
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
  "capacity": 32,
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
