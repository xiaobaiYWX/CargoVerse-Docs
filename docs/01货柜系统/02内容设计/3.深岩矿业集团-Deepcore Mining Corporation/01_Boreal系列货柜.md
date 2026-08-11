# Boreal 系列货柜设计

| 产品系列 | 规格 | 接口 | 定位 | 特点 |
| --- | --- | --- | --- | --- |
| Boreal 系列 | M/L | 【待确定】 | 矿石运输箱 | 防撞；耐磨；低成本 |

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

## DMC-Boreal-【INTERFACE】-M

### DMC Boreal 矿石运输箱 M 型

> 粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Deepcore Mining Corporation  
**系列：** Boreal Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:dmc/boreal/dmc_boreal_【interface】_m` |
| `display_name` | 显示名称 | `DMC Boreal 矿石运输箱 M 型` |
| `cargo_description` | 货柜描述 | `§lDMC Boreal 矿石运输箱 M 型\n§r§7粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：Boreal Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `M` |
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

## DMC-Boreal-【INTERFACE】-L

### DMC Boreal 矿石运输箱 L 型

> 粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Deepcore Mining Corporation  
**系列：** Boreal Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:dmc/boreal/dmc_boreal_【interface】_l` |
| `display_name` | 显示名称 | `DMC Boreal 矿石运输箱 L 型` |
| `cargo_description` | 货柜描述 | `§lDMC Boreal 矿石运输箱 L 型\n§r§7粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：Boreal Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `L` |
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
