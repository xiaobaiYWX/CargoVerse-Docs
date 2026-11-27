# VBS Harvest 保鲜货柜 X 型

> **当前状态：暂不开放，制造关闭。模板：缺本系列模板。**
> 制作安排：代号预留，当前不制作；以本页G2新版结构模板章节为准。

兼容或预留型号，制造关闭。更新于 2026-11-03。

[系列目录](<../../../绿洲农业联盟/Harvest 保鲜货柜/README.md>) · [制造商目录](<../../../绿洲农业联盟/README.md>)

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:vbs/eden_hd_x` |
| 介质 | solid |
| 尺寸 | X |
| 容量 | 480 组 |
| 定义空重 | 275 Kpg |
| 调度点 | 6 |
| 标签 | series.vbs.harvest、not_manufacturable |

实际空重取结构质量与配置空重的较大值，载荷质量另计。固体按冻结组大小计量，流体一桶为 1000 mB，生物按物种舱位确定可装只数。

## 当前保护能力

| 能力 | 参数 |
| --- | --- |
| 围护 | `level=1` |
| 密封 | `level=1` |
| 真空隔层 | `level=1`，`exchange_time_seconds=240` |
| 主动调温 | `level=1`，`target_min=2`，`target_max=40`，`rate_per_second=0.3`，`supported_modes=["cooling", "heating"]` |
| 遮光结构 | `level=1`，`reduction=15` |

完整运输条件随货物冻结，保护能力影响对应的围护、密封或内部环境求值。设备初始按需自动工作，实际降温与调压需要时间。

## G2新版结构模板

**新系列代号：`harvest_g2`；状态：代号预留，当前不制作。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/vbs/harvest_g2/vbs_harvest_g2_lm_x` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/vbs/harvest_g2/vbs_harvest_g2_lm_x.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/vbs/harvest_g2/vbs_harvest_g2_lm_x.nbt` |
| 规格／接口代号 | X／LM |
| 当前运行模板（旧版参考） | `cargoverse:cargo/aui/atlas/aui_atlas_sd_x` |
| 稳定货柜定义 ID | `cargoverse:vbs/eden_hd_x`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<../../../绿洲农业联盟/Harvest 保鲜货柜/README.md>) · [全系列新版代号](<../../../README.md#型号与模板命名>)


## 制造配方与投放

| 目录 | 许可证 | 繁荣等级 | 加工费 VB | 实体材料 |
| --- | --- | ---: | ---: | --- |
| 当前无配方 | — | — | — | — |

## 当前配置摘录

[工程定义](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/eden_hd_x.json>)。以下为现行完整定义；关闭状态不因归入正式文档而改变。

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_x",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 保鲜货柜 X 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "X",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 6,
  "capacity": 480,
  "empty_mass": 275,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.vbs.harvest",
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
      "level": 1,
      "exchange_time_seconds": 240
    },
    "cargoverse:thermal_control": {
      "level": 1,
      "target_min": 2,
      "target_max": 40,
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

[系列目录](<../../../绿洲农业联盟/Harvest 保鲜货柜/README.md>) · [制造商目录](<../../../绿洲农业联盟/README.md>)
