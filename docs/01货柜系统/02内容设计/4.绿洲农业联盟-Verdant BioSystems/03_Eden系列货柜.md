# Eden 系列货柜设计

| 产品系列    | 规格   | 接口  | 定位    | 特点         |
| ------- | ---- | --- | ----- | ---------- |
| Eden 系列 | X/XL | HD  | 生态模块舱 | 水培；温室；长期部署 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格 | CargoType 默认词条 ID                                                | 简易描述                                                                  |
| ------------------- | ------- | :--: | ---- | ---------------------------------------------------------------- | --------------------------------------------------------------------- |
| `agriculture`       | 农业产品    |  √   | X/XL | `time_limit`                                                     | 水培温室与生态循环设施适合长期生物部署，可运输谷物、蔬果、种苗等农产品。内置加压舱、控温设备以及同位素电池，可以超长时间运行，但造价昂贵。 |
| `livestock`         | 活体生物    |  √   | X/XL | `height_limit`                                                   | 水培温室与生态循环设施适合长期生物部署，可运输畜禽、育种生物及活体样本。内置加压舱、控温设备以及同位素电池，可以超长时间运行，但造价昂贵。 |
| `ore`               | 矿石资源    |  ×   | —    | 无                                                                |                                                                       |
| `wood`              | 木材      |  ×   | —    | 无                                                                |                                                                       |
| `stone`             | 石材      |  ×   | —    | 无                                                                |                                                                       |
| `fuel_resource`     | 能源原料    |  ×   | —    | `flammable`<br>`radioactive`<br>`cold_proof`                     |                                                                       |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无                                                                |                                                                       |
| `security`          | 安防与武装设备 |  ×   | —    | 无                                                                |                                                                       |
| `component`         | 工业零件    |  ×   | —    | `fragile`                                                        |                                                                       |
| `machinery`         | 机械设备    |  ×   | —    | `keep_upright`<br>`fragile`                                      |                                                                       |
| `electronics`       | 电子设备    |  ×   | —    | `moisture_proof`<br>`fragile`                                    |                                                                       |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive`                                                    |                                                                       |
| `construction`      | 建筑材料    |  ×   | —    | 无                                                                |                                                                       |
| `structural_module` | 大型结构组件  |  ×   | —    | 无                                                                |                                                                       |
| `supplies`          | 生活补给    |  ×   | —    | 无                                                                |                                                                       |
| `medical`           | 医疗物资    |  ×   | —    | `time_limit`<br>`cold_chain`<br>`light_sensitive`                |                                                                       |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile`                                      |                                                                       |
| `research_sample`   | 科研样本    |  √   | X/XL | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` | 水培温室与生态循环设施适合长期生物部署，可运输生物、地质和遗迹研究样本。内置加压舱、控温设备以及同位素电池，可以超长时间运行，但造价昂贵。 |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof`                    |                                                                       |
| `experimental`      | 实验品     |  ×   | —    | 无                                                                |                                                                       |

---

## VBS-Eden-HD-X

### VBS Eden 生态模块舱 X 型

> 集成水培、温室、环境调节和循环设施，部署后可持续培育作物并扩充聚落食物生产能力，是绿洲农业联盟的长期生态保障模块。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。

**制造商：** Verdant BioSystems  
**系列：** Eden Series  
**接口：** HD 重型保持接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                            |
| ------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/vbs/eden/vbs_eden_hd_x`                                                                                                                                                     |
| `display_name`      | 显示名称         | `VBS Eden 生态模块舱 X 型`                                                                                                                                                                          |
| `cargo_description` | 货柜描述         | `§lVBS Eden 生态模块舱 X 型\n§r§7集成水培、温室、环境调节和循环设施，部署后可持续培育作物并扩充聚落食物生产能力，是绿洲农业联盟的长期生态保障模块。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。\n§r§l制造商：Verdant BioSystems\n§r§l系列：Eden Series\n§r§l接口：HD 重型保持接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                         |
| `max_owned`         | 每个玩家的同时最大持有量 | 5                                                                                                                                                                                             |
| `cargo_level`       | 货柜等级         | `X`                                                                                                                                                                                           |
| `max_integrity`     | 最大完整性        | 70                                                                                                                                                                                            |
| `blocked_affixes`   | 屏蔽词条         | `[]`（待根据本规格货柜能力调整；填写词条 ID）                                                                                                                                                                    |

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
| `agriculture` | 5 | 2.1 | 1.5 | 0.6 | 1.5 | 1.65 |
| `livestock` | 5 | 2.3 | 1.75 | 0.4 | 1.65 | 1.75 |
| `research_sample` | 4 | 2.1 | 1.8 | 0.35 | 1.7 | 1.7 |

---

## VBS-Eden-HD-XL

### VBS Eden 生态模块舱 XL 型

> 集成水培、温室、环境调节和循环设施，部署后可持续培育作物并扩充聚落食物生产能力，是绿洲农业联盟的长期生态保障模块。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。

**制造商：** Verdant BioSystems  
**系列：** Eden Series  
**接口：** HD 重型保持接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                     |
| ------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template` | 货柜结构ID | `cargoverse:cargo/vbs/eden/vbs_eden_hd_xl` |
| `display_name` | 显示名称 | `VBS Eden 生态模块舱 XL 型` |
| `cargo_description` | 货柜描述 | `§lVBS Eden 生态模块舱 XL 型\n§r§7集成水培、温室、环境调节和循环设施，部署后可持续培育作物并扩充聚落食物生产能力，是绿洲农业联盟的长期生态保障模块。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。\n§r§l制造商：Verdant BioSystems\n§r§l系列：Eden Series\n§r§l接口：HD 重型保持接口` |
| `currency_id` | 交易物品ID | `cargoverse:enderite` |
| `max_owned` | 每个玩家的同时最大持有量 | 2 |
| `cargo_level` | 货柜等级 | `XL` |
| `max_integrity` | 最大完整性 | 70 |
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
| `agriculture` | 5 | 2.1 | 1.5 | 0.6 | 1.5 | 1.65 |
| `livestock` | 5 | 2.3 | 1.75 | 0.4 | 1.65 | 1.75 |
| `research_sample` | 4 | 2.1 | 1.8 | 0.35 | 1.7 | 1.7 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
