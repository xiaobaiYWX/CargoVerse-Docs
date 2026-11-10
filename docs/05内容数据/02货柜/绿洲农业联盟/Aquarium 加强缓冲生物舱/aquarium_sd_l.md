# VBS Aquarium 加强缓冲生物舱 L 型

> **当前状态：待模板，制造关闭。模板：缺本系列模板。**
> 制作安排：先补模板，再验证与投放。更新：2026-11-09。

> **缺失本系列模板 vbs_aquarium_sd_l.nbt，待制作。** 配方已配置，制造关闭。 更新于 2026-11-09。

## 定位与承载

加强缓冲生物舱，适用于所有已准入物种，以较少舱位与较高空重换取更强冲击保护；同系列结构模板待补齐。

| 项目 | 配置 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/aquarium_sd_l` |
| 系列／接口／规格 | aquarium／SD／L |
| 运输介质 | living，全部已准入物种 |
| 总舱位 | 48 |
| 配置空重 | 36 Kpg |
| 调度点 | 4 |
| 单体／整柜原生数据预算 | 65536／1048576 字节 |
| 模板 ID | `cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_l` |
| 模板状态 | 缺失，须补齐 cargo/vbs/aquarium/vbs_aquarium_sd_l.nbt |

装载数量取总舱位除以单只舱位的整数部分。一柜一种 EntityType，生命、名称和变种等状态随个体保存。鳕鱼和鸡都按各自物种舱位装载，牛、远古守卫者等大体型物种消耗更多舱位。实际空重取配置与结构物理质量的较大值，结构质量仍须核定。

## 能力

气密 2、隔热时间 240 秒、双向调温 5～45 TU（0.3 TU/s）、双向稳压 0.5～1.5（0.02/s）、遮光减 15。缓冲 2 级，速度变化耐受增加 5。

BioPod 采用 +2 缓冲，Aquarium 采用 +5。以冲击耐受 10 的鳕鱼为例，分别达到 12 与 15，鸡的 12 则分别达到 14 与 17。控制设备按物种需求工作，达到目标需要时间。

两系列共同承运生物。Aquarium 的空重溢价计入加强缓冲和舱体结构预算，已退出旧水体维持质量口径。现有能力参数在同系列各规格中一致，规格差异由容量、空重和材料体现。

## 制造与结构

[制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_l.json>) 按实际物品和蓝图费用配置。缺失模板期间保留 not_manufacturable 与 missing_template，模板补齐后核定结构质量和制造入口。

Aquarium 搭建重点为独立减振舱框、缓冲底座、观察窗和可维护环境设备，采用 VBS 生态设备风格与 SD 接口。外观可表现密闭观察舱，同系列 M／L 各自导出。

## 当前定义

[工程 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_l.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:vbs",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_l",
  "display_name": "VBS Aquarium 加强缓冲生物舱 L 型",
  "description": "加强缓冲生物舱，适用于所有已准入物种，以较少舱位与较高空重换取更强冲击保护；同系列结构模板待补齐。",
  "size_class": "L",
  "dispatch_points": 4,
  "empty_mass": 36,
  "allowed_cargo_classes": [
    "living"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.vbs.aquarium",
    "not_manufacturable",
    "missing_template"
  ],
  "capacity": 48,
  "abilities": {
    "cargoverse:sealing": {
      "level": 2
    },
    "cargoverse:cushioning": {
      "level": 2,
      "velocity_change_bonus": 5
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
  },
  "living_chamber": {
    "max_entity_bytes": 65536,
    "max_total_bytes": 1048576
  }
}
```

[系列目录](<README.md>) · [制造商目录](<../README.md>)

[系列目录](<README.md>) · [制造商目录](<../README.md>)
