# HEC Reactor 屏蔽危货柜 L 型


[赫利俄斯能源集团](<../README.md>) → [Reactor 屏蔽危货柜](<README.md>) → L 型

以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取屏蔽与放射性防护。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HEC-Reactor-HD-L` |
| 资源 ID | `cargoverse:hec/reactor_hd_l` |
| 定义文件 | [reactor_hd_l.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_l.json>) |
| 制造商 | 赫利俄斯能源集团 / Helios Energy Corporation（`cargoverse:hec`） |
| 系列全称 | Reactor 屏蔽危货柜 |
| 尺寸等级 | L |
| 调度点 | 4 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reactor` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hec/reactor/hec_reactor_hd_l`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reactor/hec_reactor_hd_l.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 120 | 120 |
| 空柜目标质量（Kpg） | 120 | 120 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 环境危害材料 | `hazardous_material` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：放射性、勿倒置。对应 `cargoverse:radioactive`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 800 VB |
| 实体材料 | 铁锭 ×96、黑曜石 ×32、玻璃 ×16、红石比较器 ×4 |
| 最低许可证 | L |
| 最低繁荣等级 | 2 |
| 材料最少占格 | 5 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[E03 净水与环境处理站](<../../../07_贸易点/factory/净水与环境处理站/定义设计/01_货柜制造台定义.md>)（固定专业工坊）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hec/reactor/hec_reactor_hd_l",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reactor 屏蔽危货柜 L 型",
  "description": "§lHEC Reactor 屏蔽危货柜 L 型\n§r§7以屏蔽与固定结构承运退役放射源等危险货物，较低容量换取屏蔽与放射性防护。\n§r§l制造商：赫利俄斯能源集团 / Helios Energy Corporation\n§r§l系列：Reactor 屏蔽危货柜",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 120,
  "empty_mass": 120,
  "allowed_cargo_classes": [
    "hazardous_material"
  ],
  "special_designs": [
    "cargoverse:radioactive",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.reactor"
  ]
}
```
