# HEC Apollo 温稳封装柜 L 型

> **非正式内容：关闭／兼容／预留，非正式；不列入正式型号与制作缺失数。** 核对：2026-11-06。

兼容或预留型号，制造关闭。更新于 2026-11-03。

[系列目录](<README.md>) · [制造商目录](<../../../../../05内容数据/02货柜/赫利俄斯能源集团/README.md>)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/reactor_hd_l` |
| 介质 | solid |
| 尺寸 | L |
| 容量 | 165 组 |
| 定义空重 | 190 Kpg |
| 调度点 | 4 |
| 标签 | series.hec.apollo、not_manufacturable |

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

| 核验项 | 结果 |
| --- | --- |
| 当前定义的设计系列 | `series.hec.apollo` |
| 当前运行引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_l` |
| NBT 命名的真实归属 | AUI / atlas / SD / L |
| 系列及规格是否匹配 | **否，不能作为该型号同系列模板** |
| 同系列同规格 NBT | [cargoverse:cargo/hec/apollo/hec_apollo_sd_l](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/apollo/hec_apollo_sd_l.nbt>) |
| 制作安排 | 非正式内容，不下达正式模板制作任务 |

NBT 的制造商、系列、接口和规格以目录及文件名为准；不同系列不能通过改显示名、改标签或历史合并而互相借用。缺失数按正式产品需要的系列＋规格统计，不把未规划规格算作缺失。

本轮未改 JSON 或 NBT。旧系列模板仍属于其文件名中的系列，不视为本系列资产。

[本系列正式规格](<../../../../../05内容数据/02货柜/赫利俄斯能源集团/Apollo 温稳封装柜/README.md>)

## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| 当前无配方 | — | — | — | — |

## 当前配置摘录

[工程定义](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_l.json>)。以下摘录省略旧 description 文案；产品定位以本页为准，运行字段保持工程现状。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Apollo 温稳封装柜 L 型",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 165,
  "empty_mass": 190,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.hec.apollo",
    "not_manufacturable"
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
