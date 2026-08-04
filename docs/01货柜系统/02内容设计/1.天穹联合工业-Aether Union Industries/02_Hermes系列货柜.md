# 货柜设计模板

| 产品系列     | 规格    | 接口    | 定位     | 特点                  |
| -------- | ----- | ----- | ------ | ------------------- |
| Hermes系列 | S/M/L | SD/LM | 快速物流货柜 | 快速装卸；更低的初始完整度；更轻的重量 |

## 适用货物

| CargoType           | 中文名称    | 是否可用 | 适用规格  | 词条或限制          |
| ------------------- | ------- | :--: | ----- | -------------- |
| `agriculture`       | 农业产品    |  √   | S/M/L | 限时             |
| `livestock`         | 活体生物    |  ×   |       |                |
| `ore`               | 矿石资源    |  √   | S/M/L | 无              |
| `wood`              | 木材      |  √   | S/M/L | 无              |
| `stone`             | 石材      |  √   | S/M/L | 无              |
| `fuel_resource`     | 能源原料    |  ×   |       |                |
| `textile`           | 纺织与轻工业品 |  √   | S/M/L | 无              |
| `security`          | 安防与武装设备 |  √   | S/M/L | 无              |
| `component`         | 工业零件    |  √   | S/M/L | 无              |
| `machinery`         | 机械设备    |  √   | S/M/L | 无              |
| `electronics`       | 电子设备    |  √   | S/M/L | 防潮、易碎品         |
| `chemical`          | 化工材料    |  ×   |       |                |
| `construction`      | 建筑材料    |  √   | S/M/L | 无              |
| `structural_module` | 大型结构组件  |  ×   |       |                |
| `supplies`          | 生活补给    |  √   | S/M/L | 无              |
| `medical`           | 医疗物资    |  √   | S/M/L | 冷链运输           |
| `luxury`            | 贵重消费品   |  √   | S/M/L | 易碎品、请勿倒置       |
| `research_sample`   | 科研样本    |  √   | S/M/L | 限时、易碎品、请勿倒置、避光 |
| `data`              | 数据资源    |  ×   |       |                |
| `experimental`      | 实验品     |  ×   |       |                |

---
## AUI-Vulcan-INTERFACE-S

### 【游戏内显示名称】

> 【描述该规格的定位、典型用途，以及与同系列其他规格的区别。】

**制造商：** 【Manufacturer】  
**系列：** 【Series】  
**接口：** 【Interface】

### 货柜预览截图：


### 货柜基础参数

| 参数 | 内容 |
|---|---|
| `template` | `cargoverse:【structure_template_id】` |
| `display_name` | `【游戏内显示名称】` |
| `cargo_description` | `§l【显示名称】\n§r§7【型号描述】\n§r§l制造商：【Manufacturer】\n§r§l系列：【Series】\n§r§l接口：【Interface】` |
| `currency_id` | `minecraft:emerald` |
| `max_owned` | 【待填写】 |
| `cargo_level` | `S` |
| `max_integrity` | 【待填写；无词条时不使用】 |

### 结构信息

| 项目       | 内容          |
| -------- | ----------- |
| 模板尺寸     | 【X × Y × Z】 |
| 体积       | 【待填写】       |
| 质量占位方块数量 | 【待填写】       |
| 结构基本质量   | 【待填写】       |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。
> 表内质量、价格和经验表示策划目标最终值；实际 JSON 只填写 `weight`、可选的四项微调倍率与 `affixes`，再由统一货物类型常量和货柜等级倍率反算或生成最终值。


| CargoType | `weight` | `mass_modifier` | `price_modifier` | `license_modifier` | `prosperity_modifier` | `affixes` |
|---|---:|---:|---:|---:|---:|---|
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 【无或词条及参数】 |

---

## 【MFG-MODEL-INTERFACE-M】

### 【游戏内显示名称】

> 【描述该规格的定位、典型用途，以及与同系列其他规格的区别。】

**制造商：** 【Manufacturer】  
**系列：** 【Series】  
**接口：** 【Interface】

### 货柜预览截图：


### 货柜基础参数

| 参数 | 内容 |
|---|---|
| `template` | `cargoverse:【structure_template_id】` |
| `display_name` | `【游戏内显示名称】` |
| `cargo_description` | `§l【显示名称】\n§r§7【型号描述】\n§r§l制造商：【Manufacturer】\n§r§l系列：【Series】\n§r§l接口：【Interface】` |
| `currency_id` | `minecraft:emerald` |
| `max_owned` | 【待填写】 |
| `cargo_level` | `M` |
| `max_integrity` | 【待填写；无词条时不使用】 |

### 结构信息

| 项目       | 内容          |
| -------- | ----------- |
| 模板尺寸     | 【X × Y × Z】 |
| 体积       | 【待填写】       |
| 质量占位方块数量 | 【待填写】       |
| 结构基本质量   | 【待填写】       |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。
> 表内质量、价格和经验表示策划目标最终值；实际 JSON 只填写 `weight`、可选的四项微调倍率与 `affixes`，再由统一货物类型常量和货柜等级倍率反算或生成最终值。

| CargoType | `weight` | `mass_modifier` | `price_modifier` | `license_modifier` | `prosperity_modifier` | `affixes` |
|---|---:|---:|---:|---:|---:|---|
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 【无或词条及参数】 |

---

> 继续增加 L、X、XL 或 SP 规格时，复制上方任意一个规格章节并修改 `cargo_level`。

[返回货柜内容设计](README.md)
