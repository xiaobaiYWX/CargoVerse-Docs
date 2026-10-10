# DMC Boreal 矿冶散料柜 L 型


[深岩矿业集团](<../README.md>) → [Boreal 矿冶散料柜](<README.md>) → L 型

承运原矿、精矿和冶炼材料，结合矿业承载设计与耐用结构服务矿冶供应链。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `DMC-Boreal-SD-L` |
| 资源 ID | `cargoverse:dmc/boreal_sd_l` |
| 定义文件 | [boreal_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/dmc/boreal_sd_l.json>) |
| 制造商 | 深岩矿业集团 / Deepcore Mining Corporation（`cargoverse:dmc`） |
| 系列全称 | Boreal 矿冶散料柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.dmc.boreal` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/dmc/boreal/dmc_boreal_sd_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/dmc/boreal/dmc_boreal_sd_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 240 | 240 |
| 空柜目标质量（Kpg） | 114.4 | 114.4 |

| 容量修正分类 | CargoClass | 倍率 | 实际容量（t） |
| --- | --- | ---: | ---: |
| 原始资源 | `raw_resource` | 1.3 | 312 |

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 原始资源 | `raw_resource` | 4 |
| 半成品资源 | `processed_resource` | 4 |
| 精加工资源 | `refined_resource` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 360 VB |
| 实体材料 | 铁锭 ×80、铜锭 ×32、锁链 ×16、红石 ×8 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 5 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[D03 重工材料与矿机厂](<../../../07_贸易点/factory/重工材料与矿机厂/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/dmc/boreal/dmc_boreal_sd_l",
  "manufacturer": "cargoverse:dmc",
  "display_name": "DMC Boreal 矿冶散料柜 L 型",
  "description": "§lDMC Boreal 矿冶散料柜 L 型\n§r§7承运原矿、精矿和冶炼材料，结合矿业承载设计与耐用结构服务矿冶供应链。\n§r§l制造商：深岩矿业集团 / Deepcore Mining Corporation\n§r§l系列：Boreal 矿冶散料柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 240,
  "empty_mass": 114.4,
  "allowed_cargo_classes": [
    "raw_resource",
    "processed_resource",
    "refined_resource"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.dmc.boreal"
  ],
  "cargo_class_capacity_modifiers": {
    "raw_resource": 1.3
  }
}
```
