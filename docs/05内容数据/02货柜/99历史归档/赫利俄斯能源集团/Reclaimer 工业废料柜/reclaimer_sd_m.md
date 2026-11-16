# HEC Reclaimer 工业废料柜 M 型

## G2新版结构模板

**新系列代号：`reclaimer_g2`；状态：代号预留，当前不制作。** 更新：2026-11-12。

| 项目 | 路径／约定 |
| --- | --- |
| 新版模板资源 ID | `cargoverse:cargo/hec/reclaimer_g2/hec_reclaimer_g2_sd_m` |
| 游戏导出相对路径 | `generated/cargoverse/structures/cargo/hec/reclaimer_g2/hec_reclaimer_g2_sd_m.nbt` |
| 工程目标相对路径 | `data/cargoverse/structure/cargo/hec/reclaimer_g2/hec_reclaimer_g2_sd_m.nbt` |
| 规格／接口代号 | M／SD |
| 当前运行模板（旧版参考） | `cargoverse:cargo/aui/atlas/aui_atlas_sd_m` |
| 稳定货柜定义 ID | `cargoverse:hec/reclaimer_sd_m`（保留） |

新版均尚未制作或接入。**后续搭建只按本节G2路径命名；旧路径仅用于核对当前运行状态，不再作为补建任务。** 本轮不指定长宽高、轨距或接口坐标，需在标准化尺寸表确认后搭建；接口代号目前沿系列既定命名保留，不代表几何标准已完成。

完成新模板后逐型号核对标记、归属、对接与结构质量，再切换运行 `template`；缺失模板型号须同时完成验收及制造开放。基础变体共用普通型号同规格G2模板。关闭兼容定义不自动启用。

[本系列目录](<README.md>) · [全系列新版代号](<../../../新版模板系列代号.md>)

> **当前状态：暂不开放，制造关闭。模板：已有本系列模板，引用待调整。**
> 制作安排：代号预留，当前不制作；以本页G2新版结构模板章节为准。

## 定义与承载

| 项目 | 当前值 |
| --- | --- |
| 资源 ID | `cargoverse:hec/reclaimer_sd_m` |
| 介质 | solid |
| 规格 | M |
| 容量 | 0 组 |
| 定义空重 | 64 Kpg |
| 调度点 | 2 |

## 当前配置

[工程定义](<../../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reclaimer_sd_m.json>)

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reclaimer 工业废料柜 M 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。 本期未开放该内容形态。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "empty_mass": 64,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.hec.reclaimer",
    "not_manufacturable",
    "deferred_content"
  ],
  "cargo_class_capacity_modifiers": {},
  "capacity": 0,
  "abilities": {}
}
```

[系列目录](<README.md>) · [制造商目录](<../../../赫利俄斯能源集团/README.md>)
