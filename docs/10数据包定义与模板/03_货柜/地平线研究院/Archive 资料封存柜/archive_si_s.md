# HRI Archive 资料封存柜 S 型


[地平线研究院](<../README.md>) → [Archive 资料封存柜](<README.md>) → S 型

为地平线研究院封存资料、文物与异常介质，采用缓冲、防潮、遮光及固定设计。

## 定义

| 项目 | 内容 |
| --- | --- |
| 完整型号 | `HRI-Archive-SI-S` |
| 资源 ID | `cargoverse:hri/archive_si_s` |
| 定义文件 | [archive_si_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/archive_si_s.json>) |
| 制造商 | 地平线研究院 / Horizon Research Institute（`cargoverse:hri`） |
| 系列全称 | Archive 资料封存柜 |
| 尺寸等级 | S |
| 调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hri.archive` |

## 结构模板

**正式模板已提供。** 当前引用：`cargoverse:cargo/hri/archive/hri_archive_si_s`。结构文件存在，尚未在本轮重新验证游戏内碰撞、接口与实际质量。

[当前 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/archive/hri_archive_si_s.nbt>) · [缺失模板总表](<../../缺失结构模板.md>)

## 数值

| 指标 | 定义基础值 | 实际值 |
| --- | ---: | ---: |
| 容量（t） | 32 | 32 |
| 空柜目标质量（Kpg） | 33 | 33 |

未配置 CargoClass 容量修正，所有允许分类均使用基础容量。

容量、空重、防护与缺陷均由本货柜型号直接定义；未列出的允许分类使用基础容量。指定分类容量在最终乘算后一次向下取整。目标空重仍受结构中非货柜方块质量下限约束。

## CargoClass 兼容

| 分类 | CargoClass | 当前 CargoGood 数 |
| --- | --- | --- |
| 电子设备 | `electronics` | 6 |
| 贵重物品 | `valuables` | 4 |
| 异常货物 | `anomalous_cargo` | 4 |

仅允许上表分类，`none` 与其他未列出分类均不可装载。同一允许分类下的货物均可选择，但不能混装不同 CargoGood。

## 防护与运输要求

消除：易碎、防潮、避光、勿倒置。对应 `cargoverse:fragile`、`cargoverse:moisture_proof`、`cargoverse:light_sensitive`、`cargoverse:keep_upright`。

设计缺陷：无。未被消除的货物运输要求继续生效；所有型号保留 `time_limit`。御寒不代表恒温冷藏，防潮不代表抗腐蚀。

## 制造与投放

| 项目 | v2 实体材料设计 |
| --- | --- |
| 加工费 | 200 VB |
| 实体材料 | 铁锭 ×12、玻璃 ×8、紫水晶碎片 ×4、红石比较器 ×1 |
| 最低许可证 | S |
| 最低繁荣等级 | 0 |
| 材料最少占格 | 4 格，按每种物品 64 堆叠 |
| 当前配方状态 | 配方设计完成，尚未写入运行时制造定义 |

正式提供节点：[H02 精密电子与测绘中心](<../../../07_贸易点/factory/精密电子与测绘中心/定义设计/01_货柜制造台定义.md>)（固定专业工坊）、[H03 虚空相位研究站](<../../../07_贸易点/resource/虚空相位研究站/定义设计/01_货柜制造台定义.md>)（固定配套制造台）。同型号跨站使用同一实体配方、加工费和门槛；玩家背包供料，不扣贸易点库存。普通资产按当前型号占用调度点，基础领取独立处理。

[统一配方与定价依据](<../../../08_货柜制造台/制造配方与投放总表.md>)。数值为首轮设计目标，尚未完成实机平衡。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/hri/archive/hri_archive_si_s",
  "manufacturer": "cargoverse:hri",
  "display_name": "HRI Archive 资料封存柜 S 型",
  "description": "§lHRI Archive 资料封存柜 S 型\n§r§7为地平线研究院封存资料、文物与异常介质，采用缓冲、防潮、遮光及固定设计。\n§r§l制造商：地平线研究院 / Horizon Research Institute\n§r§l系列：Archive 资料封存柜",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 32,
  "empty_mass": 33,
  "allowed_cargo_classes": [
    "electronics",
    "valuables",
    "anomalous_cargo"
  ],
  "special_designs": [
    "cargoverse:fragile",
    "cargoverse:moisture_proof",
    "cargoverse:light_sensitive",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hri.archive"
  ]
}
```
