# Harvest 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列       | 规格  | 接口  | 定位    | 特点      |
| ---------- | --- | --- | ----- | ------- |
| Harvest 系列 | M/L | LM  | 农业运输箱 | 大容量；低成本 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格 | CargoType 默认词条 ID                                                | 简易描述                                                    |
| ------------------- | ------- | :--: | ---- | ---------------------------------------------------------------- | ------------------------------------------------------- |
| `agriculture`       | 农业产品    |  √   | M/L  | `time_limit`                                                     | 大容量、易清洁结构适合农产周转，可运输谷物、蔬果、种苗等农产品。                        |
| `livestock`         | 活体生物    |  √   | M/L  | `height_limit`                                                   | 大容量、易清洁结构适合农产周转，可兼容运输活体生物，但由于没有配备BioPod的加压系统所以有不易在高空运输。 |
| `ore`               | 矿石资源    |  ×   | —    | 无                                                                |                                                         |
| `wood`              | 木材      |  ×   | —    | 无                                                                |                                                         |
| `stone`             | 石材      |  ×   | —    | 无                                                                |                                                         |
| `fuel_resource`     | 能源原料    |  ×   | —    | `flammable`<br>`radioactive`<br>`cold_proof`                     |                                                         |
| `textile`           | 纺织与轻工业品 |  √   | M/L  | 无                                                                | 大容量、易清洁结构适合农产周转，可运输布匹、纤维原料和轻工业制品。                       |
| `security`          | 安防与武装设备 |  ×   | —    | 无                                                                |                                                         |
| `component`         | 工业零件    |  ×   | —    | `fragile`                                                        |                                                         |
| `machinery`         | 机械设备    |  ×   | —    | `keep_upright`<br>`fragile`                                      |                                                         |
| `electronics`       | 电子设备    |  ×   | —    | `moisture_proof`<br>`fragile`                                    |                                                         |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive`                                                    |                                                         |
| `construction`      | 建筑材料    |  ×   | —    | 无                                                                |                                                         |
| `structural_module` | 大型结构组件  |  ×   | —    | 无                                                                |                                                         |
| `supplies`          | 生活补给    |  √   | M/L  | 无                                                                | 大容量、易清洁结构适合农产周转，可运输食品、工具和聚落日常补给。                        |
| `medical`           | 医疗物资    |  ×   | —    | `time_limit`<br>`cold_chain`<br>`light_sensitive`                |                                                         |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile`                                      |                                                         |
| `research_sample`   | 科研样本    |  ×   | —    | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |                                                         |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof`                    |                                                         |
| `experimental`      | 实验品     |  ×   | —    | 无                                                                |                                                         |

---

## VBS-Harvest-LM-M

### VBS Harvest 农业运输箱 M 型

> 为谷物、蔬果和日常口粮提供易清洁、便于通风与批量堆放的经济型空间，连接农场、集市及聚落仓储的高频农业运输。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Verdant BioSystems  
**系列：** Harvest Series  
**接口：** LM 绑扎固定

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                         |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `template`          | 货柜结构ID       | `cargoverse:cargo/vbs/harvest/vbs_harvest_lm_m`                                                                                                                                            |
| `display_name`      | 显示名称         | `VBS Harvest 农业运输箱 M 型`                                                                                                                                                                    |
| `cargo_description` | 货柜描述         | `§lVBS Harvest 农业运输箱 M 型\n§r§7为谷物、蔬果和日常口粮提供易清洁、便于通风与批量堆放的经济型空间，连接农场、集市及聚落仓储的高频农业运输。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Verdant BioSystems\n§r§l系列：Harvest Series\n§r§l接口：LM 绑扎固定` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                      |
| `max_owned`         | 每个玩家的同时最大持有量 | 5                                                                                                                                                                                          |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                        |
| `max_integrity`     | 最大完整性        | 90                                                                                                                                                                                         |
| `blocked_affixes`   | 屏蔽词条         | `time_limit`                                                                                                                                                                               |
| `base_affixes`      | 货柜基础词条       | `cold_proof`                                                                                                                                                                               |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 8 × 5 × 7 |
| 体积 | 280 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 28 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `agriculture` | 5 | 0.8 | 1.15 | 1.45 | 1.0 | 1.35 |
| `livestock` | 2 | 1.0 | 1.05 | 0.9 | 1.2 | 1.2 |
| `textile` | 2 | 0.8 | 1.05 | 1.3 | 1.0 | 1.2 |
| `supplies` | 4 | 0.8 | 1.1 | 1.4 | 1.0 | 1.3 |

---

## VBS-Harvest-LM-L

### VBS Harvest 农业运输箱 L 型

> 为谷物、蔬果和日常口粮提供易清洁、便于通风与批量堆放的经济型空间，连接农场、集市及聚落仓储的高频农业运输。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Verdant BioSystems  
**系列：** Harvest Series  
**接口：** LM 绑扎固定

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                        |
| ------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/vbs/harvest/vbs_harvest_lm_l`                                                                                                                                           |
| `display_name`      | 显示名称         | `VBS Harvest 农业运输箱 L 型`                                                                                                                                                                   |
| `cargo_description` | 货柜描述         | `§lVBS Harvest 农业运输箱 L 型\n§r§7为谷物、蔬果和日常口粮提供易清洁、便于通风与批量堆放的经济型空间，连接农场、集市及聚落仓储的高频农业运输。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Verdant BioSystems\n§r§l系列：Harvest Series\n§r§l接口：LM 绑扎固定` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                     |
| `max_owned`         | 每个玩家的同时最大持有量 | 2                                                                                                                                                                                         |
| `cargo_level`       | 货柜等级         | `L`                                                                                                                                                                                       |
| `max_integrity`     | 最大完整性        | 90                                                                                                                                                                                        |
| `blocked_affixes`   | 屏蔽词条         | `time_limit`                                                                                                                                                                              |
| `base_affixes`      | 货柜基础词条       | `cold_proof`                                                                                                                                                                              |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 13 × 6 × 8 |
| 体积 | 624 |
| 质量占位方块数量 | 4 |
| 结构基本质量 | 63 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `agriculture` | 5 | 0.8 | 1.15 | 1.45 | 1.0 | 1.35 |
| `livestock` | 2 | 1.0 | 1.05 | 0.9 | 1.2 | 1.2 |
| `textile` | 2 | 0.8 | 1.05 | 1.3 | 1.0 | 1.2 |
| `supplies` | 4 | 0.8 | 1.1 | 1.4 | 1.0 | 1.3 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
