# AUI Nomad 拓殖工程柜 L 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[天穹联合工业](<../README.md>) → [Nomad 拓殖工程柜](<README.md>) → L 型

承运拓殖设施、工程建材与部署物资，采用缓冲、防潮与固定设计，适合中小型工程交付。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Nomad-HD-L` |
| 资源 ID | `cargoverse:aui/nomad_hd_l` |
| 定义文件 | [nomad_hd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/nomad_hd_l.json>) |
| 制造商 | 天穹联合工业 / Aether Union Industries（`cargoverse:aui`） |
| 系列全称 | Nomad 拓殖工程柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.nomad` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/nomad/aui_nomad_hd_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/nomad/aui_nomad_hd_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 176 | 176 |
| 空柜目标质量（Kpg） | 112 | 112 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 建筑构件 | `construction_material` |
| 机械设备 | `machinery` |
| 物流与仓储 | `logistics_equipment` |
| 通用物资 | `general_supplies` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：易碎、防潮、勿倒置。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 560 VB |
| 实体材料 | 铁锭 ×80、橡木木板 ×32、锁链 ×16、活塞 ×4 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 5 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[A01 标准建材装配港](<../../../07_贸易点/factory/标准建材装配港/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/nomad/aui_nomad_hd_l",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Nomad 拓殖工程柜 L 型",
  "description": "§lAUI Nomad 拓殖工程柜 L 型\n§r§7承运拓殖设施、工程建材与部署物资，采用缓冲、防潮与固定设计，适合中小型工程交付。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Nomad 拓殖工程柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 176,
  "empty_mass": 112,
  "allowed_cargo_classes": [
    "construction_material",
    "machinery",
    "logistics_equipment",
    "general_supplies"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.aui.nomad"
  ]
}
```
