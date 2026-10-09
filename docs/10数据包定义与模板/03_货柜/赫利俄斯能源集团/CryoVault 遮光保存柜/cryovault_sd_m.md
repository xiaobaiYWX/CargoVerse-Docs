# HEC CryoVault 遮光保存柜 M 型


[赫利俄斯能源集团](<../README.md>) → [CryoVault 遮光保存柜](<README.md>) → M 型

通过遮光、防潮与固定设计保存敏感试剂、药品和样本，适合需要被动环境保护的运输。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-CryoVault-SD-M` |
| 资源 ID | `cargoverse:hec/cryovault_sd_m` |
| 定义文件 | [cryovault_sd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_m.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | CryoVault 遮光保存柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.cryovault` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hec/cryovault/hec_cryovault_sd_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 80 | 80 |
| 空柜目标质量（Kpg） | 60 | 60 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量倍率属于本货柜型号；未列出的允许分类使用基础容量。空重仍应用制造商倍率。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

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

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 280 VB |
| 实体材料 | 铁锭 ×32、玻璃 ×16、白色羊毛 ×16、雪块 ×8 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[E02 工业化学品供应站](<../../../07_贸易点/factory/工业化学品供应站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[V03 绿洲生物工程站](<../../../07_贸易点/factory/绿洲生物工程站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/cryovault/hec_cryovault_sd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC CryoVault 遮光保存柜 M 型",
  "description": "§lHEC CryoVault 遮光保存柜 M 型\n§r§7通过遮光、防潮与固定设计保存敏感试剂、药品和样本，适合需要被动环境保护的运输。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：CryoVault 遮光保存柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 80,
  "empty_mass": 60,
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
