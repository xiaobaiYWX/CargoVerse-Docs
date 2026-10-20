# BDS Sentinel 安防装备柜 S 型

> 分类同步说明（2026-10-20）：本页兼容类别已更新为十四类方案。其他型号/投放规划可能保留历史设计，完整运行时定义以项目 JSON 为准；本轮不重平衡容量、质量或制造价格。


[铁壁防务集团](<../README.md>) → [Sentinel 安防装备柜](<README.md>) → S 型

承运小批安防装备、电子器件与工具，以加固结构和缓冲、防潮设计保障航线补给。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `BDS-Sentinel-MC-S` |
| 资源 ID | `cargoverse:bds/sentinel_mc_s` |
| 定义文件 | [sentinel_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/bds/sentinel_mc_s.json>) |
| 制造商 | 铁壁防务集团 / Bastion Defense Systems（`cargoverse:bds`） |
| 系列全称 | Sentinel 安防装备柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.bds.sentinel` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/bds/sentinel/bds_sentinel_mc_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/bds/sentinel/bds_sentinel_mc_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（个） | 40 | 40 |
| 空柜目标质量（Kpg） | 28 | 28 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass |
| --- | --- |
| 工具与装备 | `tools_equipment` |
| 红石与控制 | `electronics` |

仅允许上述类别，不支持 none；一柜只装一种精确物品变体。首批物品标签与运输参数已配置；未覆盖物品使用默认运输规则，不代表全部物品已经归类或平衡。

## 防护与运输要求

消除：易碎、防潮。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 140 VB |
| 实体材料 | 铁锭 ×20、皮革 ×4、锁链 ×2、红石 ×2 |
| 最低许可证 | S |
| 最低繁荣等级 | 0 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[B01 铁壁防务装备站](<../../../07_贸易点/factory/铁壁防务装备站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[B03 边境驻防补给港](<../../../07_贸易点/market/边境驻防补给港/定义设计/01_货柜制造台定义.md>)（固定配套制造台）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/bds/sentinel/bds_sentinel_mc_s",
  "manufacturer": "cargoverse:bds",
  "display_name": "BDS Sentinel 安防装备柜 S 型",
  "description": "§lBDS Sentinel 安防装备柜 S 型\n§r§7承运小批安防装备、电子器件与工具，以加固结构和缓冲、防潮设计保障航线补给。\n§r§l制造商：铁壁防务集团 / Bastion Defense Systems\n§r§l系列：Sentinel 安防装备柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 40,
  "empty_mass": 28,
  "allowed_cargo_classes": [
    "tools_equipment",
    "electronics"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.bds.sentinel"
  ]
}
```

## 基础运输权益

本型号同时作为铁壁防务集团的[初始基础货柜](<../../../05_基础货柜/bds_basic.md>)。注册终端领取的基础资产占 **0 调度点**；普通购买／制造的同型号仍占 1 点。型号 JSON 中的 `dispatch_points` 保持普通版本成本，豁免依据资产标记。
