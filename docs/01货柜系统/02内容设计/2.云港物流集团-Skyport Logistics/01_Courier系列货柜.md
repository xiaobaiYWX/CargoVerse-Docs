# Courier 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列       | 规格  | 接口  | 定位   | 特点          |
| ---------- | --- | --- | ---- | ----------- |
| Courier 系列 | S/M | MC  | 快递货柜 | 极轻；快速装卸；高周转 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格 | CargoType 默认词条 ID                                                | 简易描述                              |
| ------------------- | ------- | :--: | ---- | ---------------------------------------------------------------- | --------------------------------- |
| `agriculture`       | 农业产品    |  √   | S/M  | `time_limit` | 轻量快装结构适合小批量高频配送，可运输谷物、蔬果、种苗等农产品。  |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit` |                                   |
| `ore`               | 矿石资源    |  ×   | —    | 无 |                                   |
| `wood`              | 木材      |  ×   | —    | 无 |                                   |
| `stone`             | 石材      |  ×   | —    | 无 |                                   |
| `fuel_resource`     | 能源原料    |  √   | M    | `flammable`<br>`radioactive`<br>`cold_proof` | 可用于临时应急能源运输但没有抗辐射设计，高能电池、裂变原料。    |
| `textile`           | 纺织与轻工业品 |  √   | S/M  | 无 | 轻量快装结构适合小批量高频配送，可运输布匹、纤维原料和轻工业制品。 |
| `security`          | 安防与武装设备 |  ×   | —    | 无 |                                   |
| `component`         | 工业零件    |  √   | S/M  | `fragile` | 轻量快装结构适合小批量高频配送，可运输机械零件、备件和工业组件。  |
| `machinery`         | 机械设备    |  ×   | —    | `keep_upright`<br>`fragile` |                                   |
| `electronics`       | 电子设备    |  √   | S/M  | `moisture_proof`<br>`fragile` | 轻量快装结构适合小批量高频配送，可运输传感器、控制器和计算设备。  |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive` |                                   |
| `construction`      | 建筑材料    |  ×   | —    | 无 |                                   |
| `structural_module` | 大型结构组件  |  ×   | —    | 无 |                                   |
| `supplies`          | 生活补给    |  √   | S/M  | 无 | 轻量快装结构适合小批量高频配送，可运输食品、工具和聚落日常补给。  |
| `medical`           | 医疗物资    |  √   | S/M  | `time_limit`<br>`cold_chain`<br>`light_sensitive` | 轻量化设计导致透光率较高，可运输药品、医疗器械和急救物资。     |
| `luxury`            | 贵重消费品   |  √   | S/M  | `keep_upright`<br>`fragile` | 轻量快装结构适合小批量高频配送，可运输珠宝、艺术品和高价值消费品。 |
| `research_sample`   | 科研样本    |  ×   | —    | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |                                   |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof` |                                   |
| `experimental`      | 实验品     |  ×   | —    | 无 |                                   |

---

## SPL-Courier-MC-S

### SPL Courier 快递货柜 S 型

> 采用醒目的橙白识别涂装和轻量化快速锁止结构，服务于急件分拣、区域中转与多站点接力，是云港物流高周转网络的快递单元。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。

**制造商：** Skyport Logistics  
**系列：** Courier Series  
**接口：** MC 磁力约束

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                      |
| ------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/spl/courier/spl_courier_mc_s`                                                                                                                                         |
| `display_name`      | 显示名称         | `SPL Courier 快递货柜 S 型`                                                                                                                                                                  |
| `cargo_description` | 货柜描述         | `§lSPL Courier 快递货柜 S 型\n§r§7采用醒目的橙白识别涂装和轻量化快速锁止结构，服务于急件分拣、区域中转与多站点接力，是云港物流高周转网络的快递单元。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。\n§r§l制造商：Skyport Logistics\n§r§l系列：Courier Series\n§r§l接口：MC 磁力约束` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                   |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                      |
| `cargo_level`       | 货柜等级         | `S`                                                                                                                                                                                     |
| `max_integrity`     | 最大完整性        | 70                                                                                                                                                                                      |
| `blocked_affixes`   | 屏蔽词条         | 无                                                                                                                                                                                       |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                       |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 6 × 5 × 5 |
| 体积 | 150 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 3 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `agriculture` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `textile` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `component` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `electronics` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `supplies` | 5 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `medical` | 5 | 0.55 | 1.25 | 0.75 | 1.3 | 1.2 |
| `luxury` | 3 | 0.55 | 1.2 | 0.75 | 1.2 | 1.1 |

---

## SPL-Courier-MC-M

### SPL Courier 快递货柜 M 型

> 采用醒目的橙白识别涂装和轻量化快速锁止结构，服务于急件分拣、区域中转与多站点接力，是云港物流高周转网络的快递单元。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Skyport Logistics  
**系列：** Courier Series  
**接口：** MC 磁力约束

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                           |
| ------------------- | ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/spl/courier/spl_courier_mc_m`                                                                                                                                              |
| `display_name`      | 显示名称         | `SPL Courier 快递货柜 M 型`                                                                                                                                                                       |
| `cargo_description` | 货柜描述         | `§lSPL Courier 快递货柜 M 型\n§r§7采用醒目的橙白识别涂装和轻量化快速锁止结构，服务于急件分拣、区域中转与多站点接力，是云港物流高周转网络的快递单元。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Skyport Logistics\n§r§l系列：Courier Series\n§r§l接口：MC 磁力约束` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                        |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                           |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                          |
| `max_integrity`     | 最大完整性        | 70                                                                                                                                                                                           |
| `blocked_affixes`   | 屏蔽词条         | 无                                                                                                                                                                                            |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                            |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 8 × 6 × 6 |
| 体积 | 288 |
| 质量占位方块数量 | 4 |
| 结构基本质量 | 4 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `agriculture` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `fuel_resource` | 1 | 0.75 | 1.1 | 0.85 | 1.25 | 1.1 |
| `textile` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `component` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `electronics` | 4 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `supplies` | 5 | 0.55 | 1.05 | 0.85 | 1.1 | 1.1 |
| `medical` | 5 | 0.55 | 1.25 | 0.75 | 1.3 | 1.2 |
| `luxury` | 3 | 0.55 | 1.2 | 0.75 | 1.2 | 1.1 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
