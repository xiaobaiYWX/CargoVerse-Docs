# VBS Harvest 农鲜周转柜 L 型


[绿洲农业联盟](<../README.md>) → [Harvest 农鲜周转柜](<README.md>) → L 型

面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-Harvest-LM-L` |
| 资源 ID | `cargoverse:vbs/harvest_lm_l` |
| 定义文件 | [harvest_lm_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/harvest_lm_l.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | Harvest 农鲜周转柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.harvest` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/vbs/harvest/vbs_harvest_lm_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/harvest/vbs_harvest_lm_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 240 | 240 |
| 空柜目标质量（Kpg） | 96 | 96 |

| 容量修正分类 | CargoClass | 倍率 | 实际容量（t） |
| --- | --- | ---: | ---: |
| 农业产品 | `agriculture` | 1.25 | 300 |

容量倍率属于本货柜型号；未列出的允许分类使用基础容量。空重仍应用制造商倍率。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 农业产品 | `agriculture` | 5 |
| 水产生鲜 | `aquatic` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 日常通用补给 | `general_supplies` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：防潮。对应 `cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 360 VB |
| 实体材料 | 铁锭 ×32、橡木木板 ×48、白色羊毛 ×16、玻璃 ×16 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[V01 梯田农林站](<../../../07_贸易点/resource/梯田农林站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_l",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 农鲜周转柜 L 型",
  "description": "§lVBS Harvest 农鲜周转柜 L 型\n§r§7面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：Harvest 农鲜周转柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 240,
  "empty_mass": 96,
  "allowed_cargo_classes": [
    "agriculture",
    "aquatic",
    "processed_resource",
    "general_supplies"
  ],
  "special_designs": [
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.vbs.harvest"
  ],
  "cargo_class_capacity_modifiers": {
    "agriculture": 1.25
  }
}
```
