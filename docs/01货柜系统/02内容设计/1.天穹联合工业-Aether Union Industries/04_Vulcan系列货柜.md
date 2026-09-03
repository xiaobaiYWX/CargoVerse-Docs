# Vulcan 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列      | 规格    | 接口  | 定位     | 特点             |
| --------- | ----- | --- | ------ | -------------- |
| Vulcan 系列 | M/L/X | SD  | 工业设备运输 | 电源接口；设备固定；机械运输 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格  | CargoType 默认词条 ID                                                | 简易描述               |     |
| ------------------- | ------- | :--: | ----- | ---------------------------------------------------------------- | ------------------ | --- |
| `agriculture`       | 农业产品    |  ×   | —     | `time_limit` |                    |
| `livestock`         | 活体生物    |  ×   | —     | `height_limit` |                    |
| `ore`               | 矿石资源    |  ×   | —     | 无 |                    |
| `wood`              | 木材      |  ×   | —     | 无 |                    |
| `stone`             | 石材      |  ×   | —     | 无 |                    |
| `fuel_resource`     | 能源原料    |  ×   | —     | `flammable`<br>`radioactive`<br>`cold_proof` |                    |
| `textile`           | 纺织与轻工业品 |  ×   | —     | 无 |                    |
| `security`          | 安防与武装设备 |  √   | L/X   | 无 | 固定安防设备例如雷达、火炮、移动设施 |
| `component`         | 工业零件    |  √   | M/L/X | `fragile` |                    |
| `machinery`         | 机械设备    |  √   | M/L/X | `keep_upright`<br>`fragile` |                    |
| `electronics`       | 电子设备    |  √   | M/L/X | `moisture_proof`<br>`fragile` |                    |
| `chemical`          | 化工材料    |  ×   | —     | `radioactive` |                    |
| `construction`      | 建筑材料    |  √   | L/X   | 无 |                    |
| `structural_module` | 大型结构组件  |  √   | X     | 无 |                    |
| `supplies`          | 生活补给    |  ×   | —     | 无 |                    |
| `medical`           | 医疗物资    |  ×   | —     | `time_limit`<br>`cold_chain`<br>`light_sensitive` |                    |
| `luxury`            | 贵重消费品   |  ×   | —     | `keep_upright`<br>`fragile` |                    |
| `research_sample`   | 科研样本    |  ×   | —     | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |                    |
| `data`              | 数据资源    |  √   | M/L/X | `cold_proof`<br>`fragile`<br>`moisture_proof` | 数据服务器              |
| `experimental`      | 实验品     |  ×   | —     | 无 |                    |

---

## AUI-Vulcan-SD-M

### AUI Vulcan 工业设备运输 M 型

> 以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Aether Union Industries  
**系列：** Vulcan Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                        |
| ------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_m`                                                                                                                                                             |
| `display_name`      | 显示名称         | `AUI Vulcan 工业设备运输 M 型`                                                                                                                                                                                   |
| `cargo_description` | 货柜描述         | `§lAUI Vulcan 工业设备运输 M 型\n§r§7以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Aether Union Industries\n§r§l系列：Vulcan Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                     |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                        |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                                       |
| `max_integrity`     | 最大完整性        | 115                                                                                                                                                                                                       |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `fragile`                                                                                                                                                                                |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                         |

### 结构信息

| 项目       | 内容     |
| -------- | ------ |
| 模板尺寸 | 10 × 5 × 6 |
| 体积 | 300 |
| 质量占位方块数量 | 4 |
| 结构基本质量   | 43 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `component` | 4 | 1.6 | 1.15 | 1.0 | 1.15 | 1.2 |
| `machinery` | 5 | 1.6 | 1.2 | 1.1 | 1.25 | 1.25 |
| `electronics` | 3 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `data` | 3 | 1.6 | 1.15 | 0.85 | 1.2 | 1.1 |

---

## AUI-Vulcan-SD-L

### AUI Vulcan 工业设备运输 L 型

> 以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Aether Union Industries  
**系列：** Vulcan Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                       |
| ------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_l`                                                                                                                                                            |
| `display_name`      | 显示名称         | `AUI Vulcan 工业设备运输 L 型`                                                                                                                                                                                  |
| `cargo_description` | 货柜描述         | `§lAUI Vulcan 工业设备运输 L 型\n§r§7以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Aether Union Industries\n§r§l系列：Vulcan Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                    |
| `max_owned`         | 每个玩家的同时最大持有量 | 7                                                                                                                                                                                                        |
| `cargo_level`       | 货柜等级         | `L`                                                                                                                                                                                                      |
| `max_integrity`     | 最大完整性        | 115                                                                                                                                                                                                      |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `fragile`                                                                                                                                                                               |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                        |

### 结构信息

| 项目       | 内容     |
| -------- | ------ |
| 模板尺寸 | 15 × 6 × 7 |
| 体积 | 630 |
| 质量占位方块数量 | 2 |
| 结构基本质量   | 73.5 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `security` | 2 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `component` | 4 | 1.6 | 1.15 | 1.0 | 1.15 | 1.2 |
| `machinery` | 5 | 1.6 | 1.2 | 1.1 | 1.25 | 1.25 |
| `electronics` | 3 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `construction` | 2 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `data` | 3 | 1.6 | 1.15 | 0.85 | 1.2 | 1.1 |

---

## AUI-Vulcan-SD-X

### AUI Vulcan 工业设备运输 X 型

> 以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。

**制造商：** Aether Union Industries  
**系列：** Vulcan Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                           |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `template`          | 货柜结构ID       | `cargoverse:cargo/aui/vulcan/aui_vulcan_sd_x`                                                                                                                                                                |
| `display_name`      | 显示名称         | `AUI Vulcan 工业设备运输 X 型`                                                                                                                                                                                      |
| `cargo_description` | 货柜描述         | `§lAUI Vulcan 工业设备运输 X 型\n§r§7以标准供电接口、可调式设备固定座和工业级承载框架保护机床、动力总成及成套机械，是天穹联合工业服务聚落生产体系的专业设备载体。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。\n§r§l制造商：Aether Union Industries\n§r§l系列：Vulcan Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                        |
| `max_owned`         | 每个玩家的同时最大持有量 | 5                                                                                                                                                                                                            |
| `cargo_level`       | 货柜等级         | `X`                                                                                                                                                                                                          |
| `max_integrity`     | 最大完整性        | 115                                                                                                                                                                                                          |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `fragile`                                                                                                                                                                                   |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                            |

### 结构信息

| 项目       | 内容     |
| -------- | ------ |
| 模板尺寸 | 15 × 8 × 9 |
| 体积 | 1080 |
| 质量占位方块数量 | 4 |
| 结构基本质量   | 99 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `security` | 2 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `component` | 4 | 1.6 | 1.15 | 1.0 | 1.15 | 1.2 |
| `machinery` | 5 | 1.6 | 1.2 | 1.1 | 1.25 | 1.25 |
| `electronics` | 3 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `construction` | 2 | 1.6 | 1.05 | 1.0 | 1.1 | 1.1 |
| `structural_module` | 4 | 1.8 | 1.2 | 1.1 | 1.25 | 1.3 |
| `data` | 3 | 1.6 | 1.15 | 0.85 | 1.2 | 1.1 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
