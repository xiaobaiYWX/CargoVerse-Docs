# AUI Titan 大宗结构柜 XL 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[天穹联合工业](<../README.md>) → [Titan 大宗结构柜](<README.md>) → XL 型

面向金属、钢梁和结构模块的大宗运输，以较高装载容量承接大型工程货流。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Titan-HD-XL` |
| 资源 ID | `cargoverse:aui/titan_hd_xl` |
| 定义文件 | [titan_hd_xl.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/titan_hd_xl.json>) |
| 制造商 | 天穹联合工业 / Aether Union Industries（`cargoverse:aui`） |
| 系列全称 | Titan 大宗结构柜 |
| 尺寸等级 | XL |
| 调度点 | 8 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.titan` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/titan/aui_titan_hd_xl`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/titan/aui_titan_hd_xl.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 792 | 792 |
| 空柜目标质量（Kpg） | 300 | 300 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 原料资源 | `raw_resource` |
| 加工材料 | `processed_resource` |
| 建筑构件 | `construction_material` |
| 物流与仓储 | `logistics_equipment` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 1200 VB |
| 实体材料 | 铁锭 ×288、橡木木板 ×144、锁链 ×48、红石 ×24 |
| 最低许可证 | XL |
| 最低繁荣等级 | 4 |
| 材料最少占格 | 10 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[A01 标准建材装配港](<../../../07_贸易点/factory/标准建材装配港/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/titan/aui_titan_hd_xl",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Titan 大宗结构柜 XL 型",
  "description": "§lAUI Titan 大宗结构柜 XL 型\n§r§7面向金属、钢梁和结构模块的大宗运输，以较高装载容量承接大型工程货流。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Titan 大宗结构柜",
  "size_class": "XL",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 8,
  "capacity": 792,
  "empty_mass": 300,
  "allowed_cargo_classes": [
    "raw_resource",
    "processed_resource",
    "construction_material",
    "logistics_equipment"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.aui.titan"
  ]
}
```
