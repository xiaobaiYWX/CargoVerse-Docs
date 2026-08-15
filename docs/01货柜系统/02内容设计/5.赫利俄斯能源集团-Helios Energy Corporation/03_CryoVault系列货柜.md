# CryoVault 系列货柜设计

| 产品系列 | 规格 | 接口 | 定位 | 特点 |
| --- | --- | --- | --- | --- |
| CryoVault 系列 | S/M | 【待确定】 | 特殊化学存储 | 低温；危险材料 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType | 中文名称 | 是否可用 | 适用规格 | CargoType 默认词条 ID | 简易描述 |
| --- | --- | :---: | --- | --- | --- |
| `agriculture`       | 农业产品    |  ×   | —    | `time_limit` |                                     |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit` |                                     |
| `ore`               | 矿石资源    |  ×   | —    | 无 |                                     |
| `wood`              | 木材      |  ×   | —    | 无 |                                     |
| `stone`             | 石材      |  ×   | —    | 无 |                                     |
| `fuel_resource`     | 能源原料    |  √   | S/M  | `flammable`<br>`radioactive`<br>`cold_proof` | 冗余制冷和密封结构适合低温危险品，可运输燃料、电池材料和高能介质。   |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无 |                                     |
| `security`          | 安防与武装设备 |  ×   | —    | 无 |                                     |
| `component`         | 工业零件    |  ×   | —    | `fragile` |                                     |
| `machinery`         | 机械设备    |  ×   | —    | `keep_upright`<br>`fragile` |                                     |
| `electronics`       | 电子设备    |  ×   | —    | `moisture_proof`<br>`fragile` |                                     |
| `chemical`          | 化工材料    |  √   | S/M  | `radioactive` | 冗余制冷和密封结构适合低温危险品，可运输工业试剂、化工原料和特殊介质。 |
| `construction`      | 建筑材料    |  ×   | —    | 无 |                                     |
| `structural_module` | 大型结构组件  |  ×   | —    | 无 |                                     |
| `supplies`          | 生活补给    |  ×   | —    | 无 |                                     |
| `medical`           | 医疗物资    |  √   | S/M  | `time_limit`<br>`cold_chain`<br>`light_sensitive` | 冗余制冷和密封结构适合低温危险品，可运输药品、医疗器械和急救物资。   |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile` |                                     |
| `research_sample`   | 科研样本    |  √   | S/M  | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` | 冗余制冷和密封结构适合低温危险品，可运输生物、地质和遗迹研究样本。   |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof` |                                     |
| `experimental`      | 实验品     |  ×   | —    | 无 |                                     |

---

## HEC-CryoVault-【INTERFACE】-S

### HEC CryoVault 特殊化学存储 S 型

> 依靠冗余制冷回路和危险品密封层维持低温化学品及高活性介质的稳定状态，满足实验室和能源设施之间的特种运输要求。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。

**制造商：** Helios Energy Corporation  
**系列：** CryoVault Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:hec/cryovault/hec_cryovault_【interface】_s` |
| `display_name` | 显示名称 | `HEC CryoVault 特殊化学存储 S 型` |
| `cargo_description` | 货柜描述 | `§lHEC CryoVault 特殊化学存储 S 型\n§r§7依靠冗余制冷回路和危险品密封层维持低温化学品及高活性介质的稳定状态，满足实验室和能源设施之间的特种运输要求。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。\n§r§l制造商：Helios Energy Corporation\n§r§l系列：CryoVault Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `S` |
| `max_integrity` | 最大完整性 | 【待填写；无词条时不使用】 |
| `blocked_affixes` | 屏蔽词条 | `[]`（待根据本规格货柜能力调整；填写词条 ID） |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 【X × Y × Z】 |
| 体积 | 【待填写】 |
| 质量占位方块数量 | 【待填写】 |
| 结构基本质量 | 【待填写】 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 |

---

## HEC-CryoVault-【INTERFACE】-M

### HEC CryoVault 特殊化学存储 M 型

> 依靠冗余制冷回路和危险品密封层维持低温化学品及高活性介质的稳定状态，满足实验室和能源设施之间的特种运输要求。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Helios Energy Corporation  
**系列：** CryoVault Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:hec/cryovault/hec_cryovault_【interface】_m` |
| `display_name` | 显示名称 | `HEC CryoVault 特殊化学存储 M 型` |
| `cargo_description` | 货柜描述 | `§lHEC CryoVault 特殊化学存储 M 型\n§r§7依靠冗余制冷回路和危险品密封层维持低温化学品及高活性介质的稳定状态，满足实验室和能源设施之间的特种运输要求。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Helios Energy Corporation\n§r§l系列：CryoVault Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `M` |
| `max_integrity` | 最大完整性 | 【待填写；无词条时不使用】 |
| `blocked_affixes` | 屏蔽词条 | `[]`（待根据本规格货柜能力调整；填写词条 ID） |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 【X × Y × Z】 |
| 体积 | 【待填写】 |
| 质量占位方块数量 | 【待填写】 |
| 结构基本质量 | 【待填写】 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `【cargo_type】` | 1 | 1.0 | 1.0 | 1.0 | 1.0 | 1.0 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
