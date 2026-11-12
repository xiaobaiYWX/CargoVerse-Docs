# VBS Aquarium 加强缓冲生物舱 M 型

## G2新版结构模板

**新系列代号：`aquarium_g2`；状态：需制作G2新版模板。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/aquarium_g2/vbs_aquarium_g2_sd_m` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/vbs/aquarium_g2/vbs_aquarium_g2_sd_m.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/aquarium_g2/vbs_aquarium_g2_sd_m.nbt` |
| 规格／接口代号 | M／SD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_m` |
| 稳定货柜定义 ID | `cargoverse:vbs/aquarium_sd_m`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../新版模板系列代号.md>)

> **当前状态：待模板，制造关闭。模板：缺本系列模板。**
> 制作安排：需制作G2新版模板；以本页G2新版结构模板章节为准。

> **缺失本系列模板 vbs_aquarium_sd_m.nbt，待制作。** 配方已配置，制造关闭。 更新于 2026-11-09。

## 定位与承载

加强缓冲生物舱，适用于所有已准入物种，以较少舱位与较高空重换取更强冲击保护；同系列结构模板待补齐。

| 项目 | 配置 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/aquarium_sd_m` |
| 系列／接口／规格 | aquarium／SD／M |
| 运输介质 | living，全部已准入物种 |
| 总舱位 | 24 |
| 配置空重 | 17 Kpg |
| 调度点 | 2 |
| 单体／整柜原生数据预算 | 65536／1048576 字节 |
| 模板 ID | `cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_m` |
| 模板状态 | 缺失，须补齐 cargo/vbs/aquarium/vbs_aquarium_sd_m.nbt |

装载数量取总舱位除以单只舱位的整数部分。一柜一种 EntityType，生命、名称和变种等状态随个体保存。鳕鱼和鸡都按各自物种舱位装载，牛、远古守卫者等大体型物种消耗更多舱位。实际空重取配置与结构物理质量的较大值，结构质量仍须核定。

## 能力

气密 2、隔热时间 240 秒、双向调温 5～45 TU（0.3 TU/s）、双向稳压 0.5～1.5（0.02/s）、遮光减 15。缓冲 2 级，速度变化耐受增加 5。

BioPod 采用 +2 缓冲，Aquarium 采用 +5。以冲击耐受 10 的鳕鱼为例，分别达到 12 与 15，鸡的 12 则分别达到 14 与 17。控制设备按物种需求工作，达到目标需要时间。

两系列共同承运生物。Aquarium 的空重溢价计入加强缓冲和舱体结构预算，已退出旧水体维持质量口径。现有能力参数在同系列各规格中一致，规格差异由容量、空重和材料体现。

## 制造与结构

[制造配方](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/aquarium_sd_m.json>) 按实际物品和蓝图费用配置。缺失模板期间保留 not_manufacturable 与 missing_template，模板补齐后核定结构质量和制造入口。

Aquarium 搭建重点为独立减振舱框、缓冲底座、观察窗和可维护环境设备，采用 VBS 生态设备风格与 SD 接口。外观可表现密闭观察舱，同系列 M／L 各自导出。

## 当前定义

[工程 JSON](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/aquarium_sd_m.json>)

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:vbs",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/vbs/aquarium/vbs_aquarium_sd_m",
  "display_name": "VBS Aquarium 加强缓冲生物舱 M 型",
  "description": "加强缓冲生物舱，适用于所有已准入物种，以较少舱位与较高空重换取更强冲击保护；同系列结构模板待补齐。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 17,
  "allowed_cargo_classes": [
    "living"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.vbs.aquarium",
    "not_manufacturable",
    "missing_template"
  ],
  "capacity": 24,
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
