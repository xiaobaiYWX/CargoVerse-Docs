# HEC CryoVault 深冷货柜 L 型

兼容或预留型号，制造关闭。更新于 2026-11-03。

[系列目录](README.md) · [制造商目录](../README.md)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/cryovault_sd_l` |
| 介质 | solid |
| 尺寸 | L |
| 容量 | 210 组 |
| 定义空重 | 160 Kpg |
| 调度点 | 4 |
| 标签 | series.hec.cryovault、not_manufacturable |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 真空隔层 | `level=2`，`exchange_time_seconds=480` |
| 主动调温 | `level=3`，`target_min=-20`，`target_max=80`，`rate_per_second=0.6`，`supported_modes=["cooling", "heating"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## 结构模板
| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:hec/cryovault_sd_l](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_l.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| 当前 NBT | [Atlas L 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_l.nbt>)；包络 13×6×6，体积 468；标准对接接口×6 |
| 专用路径建议 | `cargoverse:cargo/hec/cryovault/hec_cryovault_sd_l`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**原自用模板候选：** `cargoverse:cargo/hec/cryovault/hec_cryovault_sd_l` · [原 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_l.nbt>)。

只读结构检查：包络 7×15×7；标准对接接口×4；质量占位 1 个；分类占位 4 个；警示占位 20 个（槽号 0／1／2／3／4）；实体 0 个。这不是碰撞、实际质量、密封性或 Sable 连接验收。

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| 当前无配方 | — | — | — | — |

## 当前 JSON

[工程定义](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_l.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC CryoVault 深冷货柜 L 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 210,
  "empty_mass": 160,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hec.cryovault",
    "not_manufacturable"
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
