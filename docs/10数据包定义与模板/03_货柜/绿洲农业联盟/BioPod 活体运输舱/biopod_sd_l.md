# VBS BioPod 活体运输舱 L 型

[绿洲农业联盟](<../README.md>) → [BioPod 活体运输舱](<README.md>) → L 型

通过固定与御寒设计承运活体、水产和生物相关货物，适合繁育场及生态设施补给。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `VBS-BioPod-SD-L` |
| 资源 ID | `cargoverse:vbs/biopod_sd_l` |
| 定义文件 | [biopod_sd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/biopod_sd_l.json>) |
| 制造商 | 绿洲农业联盟 / Verdant BioSystems（`cargoverse:vbs`） |
| 系列全称 | BioPod 活体运输舱 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.vbs.biopod` |

## 结构模板

**正式模板已接入。** 当前引用：`cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l`。

包络尺寸（X × Y × Z）：**11 × 6 × 7** 方块；体积 462 方块³。

模板中的连接部件：`cargoverse:cargo_docking_port` ×6。已校验压缩 NBT、尺寸、方块位置与调色板索引；游戏内连接、碰撞和实际质量尚未重新实测。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/vbs/biopod/vbs_biopod_sd_l.nbt>) · [模板接入与缺失清单](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 32 | 32 |
| 空柜目标质量（Kpg） | 120 | 120 |
| 最大耐久 | 120 | 120 |

绿洲农业联盟：当前 5 种农业货物与 4 种活体货物容量 ×1.25；水产与研究样本不享受该专项倍率。实际装载仍须满足本柜的分类许可。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 活体生物 | `livestock` | 4 |
| 水产生鲜 | `aquatic` | 4 |
| 科研样本 | `research_sample` | 4 |
| 医疗物资 | `medical_supply` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：御寒、勿倒置。对应 `cargoverse:cold_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | 值 |
| --- | --- |
| 规划加工费 | 480 VB（不含库存材料） |
| 最低许可证 | L |
| 最低繁荣等级 | 3 |
| 规划节点类型 | 育种场、水产繁育站 |
| 当前配方状态 | 待编制材料配方、绑定制造台与供应节点 |

货柜定义已注册，可供系统引用；规划加工费与门槛尚未写入制造配方，不代表现有制造台可购买该型号。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/vbs/biopod/vbs_biopod_sd_l",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS BioPod 活体运输舱 L 型",
  "description": "§lVBS BioPod 活体运输舱 L 型\n§r§7通过固定与御寒设计承运活体、水产和生物相关货物，适合繁育场及生态设施补给。\n§r§l制造商：绿洲农业联盟 / Verdant BioSystems\n§r§l系列：BioPod 活体运输舱",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 32,
  "empty_mass": 120,
  "max_durability": 120,
  "allowed_cargo_classes": [
    "livestock",
    "aquatic",
    "research_sample",
    "medical_supply"
  ],
  "special_designs": [
    "cargoverse:cold_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.vbs.biopod"
  ]
}
```
