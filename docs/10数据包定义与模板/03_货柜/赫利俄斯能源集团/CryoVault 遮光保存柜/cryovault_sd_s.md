# HEC CryoVault 遮光保存柜 S 型

[赫利俄斯能源集团](<../README.md>) → [CryoVault 遮光保存柜](<README.md>) → S 型

通过遮光、防潮与固定设计保存敏感试剂、药品和样本，适合需要被动环境保护的运输。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-CryoVault-SD-S` |
| 资源 ID | `cargoverse:hec/cryovault_sd_s` |
| 定义文件 | [cryovault_sd_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_s.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | CryoVault 遮光保存柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.cryovault` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hec/cryovault/hec_cryovault_sd_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 8 | 8 |
| 空柜目标质量（Kpg） | 30 | 30 |
| 最大耐久 | 140 | 140 |

本厂商当前无额外数值修正。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 化工原料 | `chemical_material` | 5 |
| 医疗物资 | `medical_supply` | 4 |
| 水产生鲜 | `aquatic` | 4 |
| 科研样本 | `research_sample` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：避光、防潮、勿倒置。对应 `cargoverse:light_sensitive`、`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 140 VB（不含库存材料） |
| 最低许可证 | S |
| 最低繁荣等级 | 1 |
| 规划节点类型 | 医药集散站、敏感试剂站 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/cryovault/hec_cryovault_sd_s",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC CryoVault 遮光保存柜 S 型",
  "description": "§lHEC CryoVault 遮光保存柜 S 型\n§r§7通过遮光、防潮与固定设计保存敏感试剂、药品和样本，适合需要被动环境保护的运输。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：CryoVault 遮光保存柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 8,
  "empty_mass": 30,
  "max_durability": 140,
  "allowed_cargo_classes": [
    "chemical_material",
    "medical_supply",
    "aquatic",
    "research_sample"
  ],
  "special_designs": [
    "cargoverse:light_sensitive",
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.cryovault"
  ]
}
```
