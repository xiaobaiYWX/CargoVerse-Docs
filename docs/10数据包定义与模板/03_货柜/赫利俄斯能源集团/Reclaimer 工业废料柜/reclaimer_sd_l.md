# HEC Reclaimer 工业废料柜 L 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[赫利俄斯能源集团](<../README.md>) → [Reclaimer 工业废料柜](<README.md>) → L 型

承运工业回收料与低单价大宗废物，提供固定设计及经济的大容量周转方案。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Reclaimer-SD-L` |
| 资源 ID | `cargoverse:hec/reclaimer_sd_l` |
| 定义文件 | [reclaimer_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reclaimer_sd_l.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Reclaimer 工业废料柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reclaimer` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/hec/reclaimer/hec_reclaimer_sd_l`。

包络尺寸（X × Y × Z）：**13 × 7 × 7** 方块；体积 637 方块³。

模板中的连接部件：`cargoverse:cargo_docking_port` ×6。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reclaimer/hec_reclaimer_sd_l.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 240 | 240 |
| 空柜目标质量（Kpg） | 128 | 128 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 化工与药剂 | `chemical_material` |
| 燃料与能源 | `energy_fuel` |
| 原料资源 | `raw_resource` |
| 加工材料 | `processed_resource` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：勿倒置。对应 `cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 360 VB |
| 实体材料 | 铁锭 ×64、铜锭 ×32、玻璃 ×16、皮革 ×16 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[E03 净水与环境处理站](<../../../07_贸易点/factory/净水与环境处理站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reclaimer/hec_reclaimer_sd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reclaimer 工业废料柜 L 型",
  "description": "§lHEC Reclaimer 工业废料柜 L 型\n§r§7承运工业回收料与低单价大宗废物，提供固定设计及经济的大容量周转方案。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reclaimer 工业废料柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 240,
  "empty_mass": 128,
  "allowed_cargo_classes": [
    "chemical_material",
    "energy_fuel",
    "raw_resource",
    "processed_resource"
  ],
  "special_designs": [
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.reclaimer"
  ]
}
```
