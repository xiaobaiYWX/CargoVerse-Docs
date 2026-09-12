# SPL Express 特快专递舱 S 型

[云港物流集团](<../README.md>) → [Express 特快专递舱](<README.md>) → S 型

该系列恢复原尺寸、基础数值与分类许可；制造费用尚未重新定稿。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `SPL-Express-MC-S` |
| 资源 ID | `cargoverse:spl/express_mc_s` |
| 定义文件 | [express_mc_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/express_mc_s.json>) |
| 制造商 | 云港物流集团 |
| 系列全称 | Express 特快专递舱 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.spl.express` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/spl/express/spl_express_mc_s`。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/express/spl_express_mc_s.nbt>) · [模板接入状态](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 8 | 8 |
| 空柜目标质量（Kpg） | 18 | 18 |
| 最大耐久 | 75 | 75 |

实际容量包含厂商通用倍率并向下取整；专项货物倍率另行计算。空重仍受模板中非货柜方块质量下限约束。

## CargoClass 兼容

`mechanical_parts`、`medical_supply`、`valuables`、`research_sample`、`electronics`。仅允许上述分类，不支持 none；同一货柜不可混装不同 CargoGood。

## 防护与运输要求

消除：无。

设计缺陷：无。所有货物的原有 time_limit 继续生效；御寒不代表恒温冷藏。

## 制造与投放

| 项目 | 规划 |
| --- | --- |
| 加工费 VB | 待设计 |
| 最低许可证 | S |
| 最低繁荣等级 | 1 |
| 节点类型 | 急件与精密小件交接站 |
| 当前配方 | 待编制材料配方与投放；定义已注册 |

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/spl/express/spl_express_mc_s",
  "manufacturer": "cargoverse:spl",
  "display_name": "SPL Express 特快专递舱 S 型",
  "description": "§lSPL Express 特快专递舱 S 型\n§r§7保留原有特快专递产品线，承运精密小件与高价值急件；货物原有运输要求仍需遵守。\n§r§l制造商：云港物流集团\n§r§l系列：Express 特快专递舱",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 8,
  "empty_mass": 18,
  "max_durability": 75,
  "allowed_cargo_classes": [
    "mechanical_parts",
    "medical_supply",
    "valuables",
    "research_sample",
    "electronics"
  ],
  "special_designs": [],
  "design_defects": [],
  "tags": [
    "series.spl.express"
  ]
}
```
