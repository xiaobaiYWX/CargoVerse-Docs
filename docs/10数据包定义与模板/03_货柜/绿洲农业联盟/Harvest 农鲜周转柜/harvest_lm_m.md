# VBS Harvest 农鲜周转柜 M 型


[绿洲农业联盟](<../README.md>) → [Harvest 农鲜周转柜](<README.md>) → M 型

面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-Harvest-LM-M` |
| 资源 ID | `cargoverse:vbs/harvest_lm_m` |
| 定义文件 | [harvest_lm_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/harvest_lm_m.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | Harvest 农鲜周转柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.harvest` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/vbs/harvest/vbs_harvest_lm_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/harvest/vbs_harvest_lm_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 24 | 24 |
| 空柜目标质量（Kpg） | 48 | 48 |
| 最大耐久 | 85 | 85 |

绿洲农业联盟：当前 5 种农业货物与 4 种活体货物容量 ×1.25；水产与研究样本不享受该专项倍率。实际装载仍须满足本柜的分类许可。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

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
| 加工费 | 180 VB |
| 实体材料 | 铁锭 ×16、橡木木板 ×24、白色羊毛 ×8、玻璃 ×8 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[绿洲生物工程站](<../../../07_贸易点/factory/绿洲生物工程站/货柜制造台定义.md>)（固定中心）、[梯田农林站](<../../../07_贸易点/resource/梯田农林站/货柜制造台定义.md>)（仅抽中工坊时）。同型号跨站使用同一配方与加工费。材料来自玩家随身物品栏，不扣贸易点库存；正常占用 2 调度点，基础领取另行处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/harvest/vbs_harvest_lm_m",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Harvest 农鲜周转柜 M 型",
  "description": "§lVBS Harvest 农鲜周转柜 M 型\n§r§7面向农鲜供应链的周转货柜，提供防潮保护，并发挥绿洲农业联盟的农业装载专长。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：Harvest 农鲜周转柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 24,
  "empty_mass": 48,
  "max_durability": 85,
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
  ]
}
```
