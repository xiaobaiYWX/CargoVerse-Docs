# Fortress 系列货柜设计

| 产品系列 | 规格 | 接口 | 定位 | 特点 |
| --- | --- | --- | --- | --- |
| Fortress 系列 | XL/SP | 【待确定】 | 堡垒部署模块 | 前线基地；大型装备 |

## 适用货物

> 命名规则未规定本系列适用的 CargoType；下表保留策划占位，不据产品定位擅自推定。

| CargoType | 中文名称 | 是否可用 | 适用规格 | 词条或限制 |
| --- | --- | :---: | --- | --- |
| `agriculture` | 农业产品 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `livestock` | 活体生物 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `ore` | 矿石资源 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `wood` | 木材 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `stone` | 石材 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `fuel_resource` | 能源原料 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `textile` | 纺织与轻工业品 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `security` | 安防与武装设备 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `component` | 工业零件 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `machinery` | 机械设备 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `electronics` | 电子设备 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `chemical` | 化工材料 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `construction` | 建筑材料 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `structural_module` | 大型结构组件 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `supplies` | 生活补给 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `medical` | 医疗物资 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `luxury` | 贵重消费品 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `research_sample` | 科研样本 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `data` | 数据资源 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |
| `experimental` | 实验品 | 【√/×】 | 【待填写】 | 【待填写或不可用】 |

---

## BDS-Fortress-【INTERFACE】-XL

### BDS Fortress 堡垒部署模块 XL 型

> 将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。

**制造商：** Bastion Defense Systems  
**系列：** Fortress Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:bds/fortress/bds_fortress_【interface】_xl` |
| `display_name` | 显示名称 | `BDS Fortress 堡垒部署模块 XL 型` |
| `cargo_description` | 货柜描述 | `§lBDS Fortress 堡垒部署模块 XL 型\n§r§7将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。\n§r§l制造商：Bastion Defense Systems\n§r§l系列：Fortress Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `XL` |
| `max_integrity` | 最大完整性 | 【待填写；无词条时不使用】 |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 【X × Y × Z】 |
| 体积 | 【待填写】 |
| 质量占位方块数量 | 【待填写】 |
| 结构基本质量 | 【待填写】 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际 JSON 只填写权重、可选微调倍率与词条。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` | `affixes` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | --- |
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 【无或词条及参数】 |

---

## BDS-Fortress-【INTERFACE】-SP

### BDS Fortress 堡垒部署模块 SP 型

> 将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 SP 型不按常规体积划分，将依据具体货物、设备或任务单独配置。

**制造商：** Bastion Defense Systems  
**系列：** Fortress Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:bds/fortress/bds_fortress_【interface】_sp` |
| `display_name` | 显示名称 | `BDS Fortress 堡垒部署模块 SP 型` |
| `cargo_description` | 货柜描述 | `§lBDS Fortress 堡垒部署模块 SP 型\n§r§7将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 SP 型不按常规体积划分，将依据具体货物、设备或任务单独配置。\n§r§l制造商：Bastion Defense Systems\n§r§l系列：Fortress Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `SP` |
| `max_integrity` | 最大完整性 | 【待填写；无词条时不使用】 |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 【X × Y × Z】 |
| 体积 | 【待填写】 |
| 质量占位方块数量 | 【待填写】 |
| 结构基本质量 | 【待填写】 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际 JSON 只填写权重、可选微调倍率与词条。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` | `affixes` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | --- |
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 | 【无或词条及参数】 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
