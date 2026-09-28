# AUI Vulcan 精密工业柜 M 型


[天穹联合工业](<../README.md>) → [Vulcan 精密工业柜](<README.md>) → M 型

承运工业成套设备、精密部件与载具，使用缓冲和防潮设计保护易损工业货物。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `AUI-Vulcan-SD-M` |
| 资源 ID | `cargoverse:aui/vulcan_sd_m` |
| 定义文件 | [vulcan_sd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/aui/vulcan_sd_m.json>) |
| 制造商 | 天穹联合工业 / Aether Union Industries（`cargoverse:aui`） |
| 系列全称 | Vulcan 精密工业柜 |
| 尺寸等级 | M |
| 调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.aui.vulcan` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/aui/vulcan/aui_vulcan_sd_m`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/vulcan/aui_vulcan_sd_m.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 默认实际值（含厂商通用倍率） |
| --- | --- | --- |
| 容量（t） | 16 | 17 |
| 空柜目标质量（Kpg） | 52 | 52 |
| 最大耐久 | 140 | 140 |

天穹联合工业：容量 ×1.1，空重与耐久不变。 指定货物容量按所有适用倍率相乘后一次向下取整，不能先取整默认容量再乘专项倍率。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 机械设备 | `machinery` | 4 |
| 机械零件 | `mechanical_parts` | 5 |
| 电子设备 | `electronics` | 6 |
| 精加工资源 | `refined_resource` | 4 |
| 工具器械 | `tools_equipment` | 4 |
| 完整载具 | `vehicle` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 240 VB |
| 实体材料 | 铁锭 ×32、玻璃 ×8、白色羊毛 ×8、红石比较器 ×2 |
| 最低许可证 | M |
| 最低繁荣等级 | 1 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[通用机电装备厂](<../../../07_贸易点/factory/通用机电装备厂/货柜制造台定义.md>)（固定中心）。同型号跨站使用同一配方与加工费。材料来自玩家随身物品栏，不扣贸易点库存；正常占用 2 调度点，基础领取另行处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/vulcan/aui_vulcan_sd_m",
  "manufacturer": "cargoverse:aui",
  "display_name": "AUI Vulcan 精密工业柜 M 型",
  "description": "§lAUI Vulcan 精密工业柜 M 型\n§r§7承运工业成套设备、精密部件与载具，使用缓冲和防潮设计保护易损工业货物。\n§r§l制造商：天穹联合工业 / Aether Union Industries\n§r§l系列：Vulcan 精密工业柜",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 16,
  "empty_mass": 52,
  "max_durability": 140,
  "allowed_cargo_classes": [
    "machinery",
    "mechanical_parts",
    "electronics",
    "refined_resource",
    "tools_equipment",
    "vehicle"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.aui.vulcan"
  ]
}
```
