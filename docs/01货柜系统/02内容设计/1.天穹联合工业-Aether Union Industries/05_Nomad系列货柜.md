# Nomad 系列货柜设计

| 产品系列     | 规格  | 接口  | 定位     | 特点           |
| -------- | --- | --- | ------ | ------------ |
| Nomad 系列 | L/X | HD  | 野外部署模块 | 临时基地；科考；前线补给 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType | 中文名称 | 是否可用 | 适用规格 | CargoType 默认词条 ID | 简易描述 |
| --- | --- | :---: | --- | --- | --- |
| `agriculture`       | 农业产品    |  ×   | —    | `time_limit` |                                      |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit` |                                      |
| `ore`               | 矿石资源    |  ×   | —    | 无 |                                      |
| `wood`              | 木材      |  ×   | —    | 无 |                                      |
| `stone`             | 石材      |  ×   | —    | 无 |                                      |
| `fuel_resource`     | 能源原料    |  ×   | —    | `flammable`<br>`radioactive`<br>`cold_proof` |                                      |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无 |                                      |
| `security`          | 安防与武装设备 |  ×   | —    | 无 |                                      |
| `component`         | 工业零件    |  ×   | —    | `fragile` |                                      |
| `machinery`         | 机械设备    |  √   | L/X  | `keep_upright`<br>`fragile` | 野外部署结构可随基地运输配套物资，可运输机床、动力设备和工程机械。    |
| `electronics`       | 电子设备    |  √   | L/X  | `moisture_proof`<br>`fragile` | 野外部署结构可随基地运输配套物资，可运输传感器、控制器和计算设备。    |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive` |                                      |
| `construction`      | 建筑材料    |  √   | L/X  | 无 | 野外部署结构可随基地运输配套物资，可运输建材、管线和设施配套材料。    |
| `structural_module` | 大型结构组件  |  √   | X    | 无 | 野外部署结构可随基地运输配套物资，可运输预制舱段、设备模块和大型结构件。 |
| `supplies`          | 生活补给    |  √   | L/X  | 无 | 野外部署结构可随基地运输配套物资，可运输食品、工具和聚落日常补给。    |
| `medical`           | 医疗物资    |  √   | L/X  | `time_limit`<br>`cold_chain`<br>`light_sensitive` | 野外部署结构可随基地运输配套物资，可运输药品、医疗器械和急救物资。    |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile` |                                      |
| `research_sample`   | 科研样本    |  √   | L/X  | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` | 野外部署结构可随基地运输配套物资，可运输生物、地质和遗迹研究样本。    |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof` |                                      |
| `experimental`      | 实验品     |  ×   | —    | 无 |                                      |

---

## AUI-Nomad-【INTERFACE】-L

### AUI Nomad 野外部署模块 L 型

> 将标准货柜改造成具备基础供能、物资组织与环境防护能力的部署单元，供科考队、维修队和远征人员快速建立临时据点。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Aether Union Industries  
**系列：** Nomad Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:aui/nomad/aui_nomad_【interface】_l` |
| `display_name` | 显示名称 | `AUI Nomad 野外部署模块 L 型` |
| `cargo_description` | 货柜描述 | `§lAUI Nomad 野外部署模块 L 型\n§r§7将标准货柜改造成具备基础供能、物资组织与环境防护能力的部署单元，供科考队、维修队和远征人员快速建立临时据点。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Aether Union Industries\n§r§l系列：Nomad Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `L` |
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

## AUI-Nomad-【INTERFACE】-X

### AUI Nomad 野外部署模块 X 型

> 将标准货柜改造成具备基础供能、物资组织与环境防护能力的部署单元，供科考队、维修队和远征人员快速建立临时据点。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。

**制造商：** Aether Union Industries  
**系列：** Nomad Series  
**接口：** 【待确定】

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数 | 名称 | 内容 |
| --- | --- | --- |
| `template` | 货柜结构ID | `cargoverse:aui/nomad/aui_nomad_【interface】_x` |
| `display_name` | 显示名称 | `AUI Nomad 野外部署模块 X 型` |
| `cargo_description` | 货柜描述 | `§lAUI Nomad 野外部署模块 X 型\n§r§7将标准货柜改造成具备基础供能、物资组织与环境防护能力的部署单元，供科考队、维修队和远征人员快速建立临时据点。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。\n§r§l制造商：Aether Union Industries\n§r§l系列：Nomad Series\n§r§l接口：【待确定】` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 【待填写】 |
| `cargo_level` | 货柜等级 | `X` |
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
