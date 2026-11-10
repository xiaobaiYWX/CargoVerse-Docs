# VBS BioPod 通用生物舱 L 型

> **当前状态：待实运验证，可制造。模板：本系列模板已绑定。**
> 制作安排：装配、对接与满载运输待实机验证。更新：2026-11-09。

> 本系列同规格模板已绑定。现属验证投放型号。 更新于 2026-11-09。

## 定位与承载

通用生物运输舱，提供调温、稳压、遮光与基础缓冲，适用于所有已准入物种。

| 项目 | 配置 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/biopod_sd_l` |
| 系列／接口／规格 | biopod／SD／L |
| 运输介质 | living，全部已准入物种 |
| 总舱位 | 64 |
| 配置空重 | 30 Kpg |
| 调度点 | 4 |
| 单体／整柜原生数据预算 | 65536／1048576 字节 |
| 模板 ID | `cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l` |
| 模板状态 | 同系列、同规格，文件存在并已绑定 |

装载数量取总舱位除以单只舱位的整数部分。一柜一种 EntityType，生命、名称和变种等状态随个体保存。鳕鱼和鸡都按各自物种舱位装载，牛、远古守卫者等大体型物种消耗更多舱位。实际空重取配置与结构物理质量的较大值，结构质量仍须核定。

## 能力

气密 2、隔热时间 240 秒、双向调温 5～45 TU（0.3 TU/s）、双向稳压 0.5～1.5（0.02/s）、遮光减 15。缓冲 1 级，速度变化耐受增加 2。

BioPod 采用 +2 缓冲，Aquarium 采用 +5。以冲击耐受 10 的鳕鱼为例，分别达到 12 与 15，鸡的 12 则分别达到 14 与 17。控制设备按物种需求工作，达到目标需要时间。

两系列共同承运生物。Aquarium 的空重溢价计入加强缓冲和舱体结构预算，已退出旧水体维持质量口径。现有能力参数在同系列各规格中一致，规格差异由容量、空重和材料体现。

## 制造与结构

[制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/biopod_sd_l.json>) 按实际物品和蓝图费用配置。现有测试目录与自然站渠道沿定义读取本型号。

BioPod 使用自身 biopod 系列 S／M／L NBT，当前定义已与对应文件一致。

## 当前定义

[工程 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_l.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 通用生物舱 L 型",
  "description": "通用生物运输舱，提供调温、稳压、遮光与基础缓冲，适用于所有已准入物种。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "empty_mass": 30,
  "allowed_cargo_classes": [
    "living"
  ],
  "tags": [
    "series.vbs.biopod",
    "validation_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 64,
  "living_chamber": {
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

[系列目录](<README.md>) · [制造商目录](<../README.md>)

[系列目录](<README.md>) · [制造商目录](<../README.md>)
