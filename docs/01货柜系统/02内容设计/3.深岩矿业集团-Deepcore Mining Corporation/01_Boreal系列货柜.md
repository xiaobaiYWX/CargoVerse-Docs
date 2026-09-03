# Boreal 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列      | 规格  | 接口  | 定位    | 特点        |
| --------- | --- | --- | ----- | --------- |
| Boreal 系列 | M/L | SD  | 矿石运输箱 | 防撞；耐磨；低成本 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格 | CargoType 默认词条 ID                                                | 简易描述                          |
| ------------------- | ------- | :--: | ---- | ---------------------------------------------------------------- | ----------------------------- |
| `agriculture`       | 农业产品    |  ×   | —    | `time_limit`                                                     |                               |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit`                                                   |                               |
| `ore`               | 矿石资源    |  √   | M/L  | 无                                                                | 耐磨防撞箱体适合粗放装卸，可运输原矿、精炼矿料和稀有矿石。 |
| `wood`              | 木材      |  ×   | —    | 无                                                                |                               |
| `stone`             | 石材      |  √   | M/L  | 无                                                                | 耐磨防撞箱体适合粗放装卸，可运输石料、砖材和矿区岩样。   |
| `fuel_resource`     | 能源原料    |  ×   | —    | `flammable`<br>`radioactive`<br>`cold_proof`                     |                               |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无                                                                |                               |
| `security`          | 安防与武装设备 |  ×   | —    | 无                                                                |                               |
| `component`         | 工业零件    |  ×   | —    | `fragile`                                                        |                               |
| `machinery`         | 机械设备    |  √   | M/L  | `keep_upright`<br>`fragile`                                      | 耐磨防撞箱体适合粗放装卸，可运轻型开采设备。        |
| `electronics`       | 电子设备    |  ×   | —    | `moisture_proof`<br>`fragile`                                    |                               |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive`                                                    |                               |
| `construction`      | 建筑材料    |  ×   | —    | 无                                                                |                               |
| `structural_module` | 大型结构组件  |  ×   | —    | 无                                                                |                               |
| `supplies`          | 生活补给    |  ×   | —    | 无                                                                |                               |
| `medical`           | 医疗物资    |  ×   | —    | `time_limit`<br>`cold_chain`<br>`light_sensitive`                |                               |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile`                                      |                               |
| `research_sample`   | 科研样本    |  ×   | —    | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |                               |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof`                    |                               |
| `experimental`      | 实验品     |  ×   | —    | 无                                                                |                               |

---

## DMC-Boreal-SD-M

### DMC Boreal 矿石运输箱 M 型

> 粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Deepcore Mining Corporation  
**系列：** Boreal Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                      |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/dmc/boreal/dmc_boreal_sd_m`                                                                                                                                                           |
| `display_name`      | 显示名称         | `DMC Boreal 矿石运输箱 M 型`                                                                                                                                                                                  |
| `cargo_description` | 货柜描述         | `§lDMC Boreal 矿石运输箱 M 型\n§r§7粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：Boreal Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                   |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                      |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                                     |
| `max_integrity`     | 最大完整性        | 130                                                                                                                                                                                                     |
| `blocked_affixes`   | 屏蔽词条         | 无                                                                                                                                                                                                       |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                       |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 10 × 6 × 5 |
| 体积 | 300 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 10 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `ore` | 5 | 1.9 | 1.25 | 1.25 | 1.2 | 1.3 |
| `stone` | 4 | 1.8 | 1.2 | 1.2 | 1.15 | 1.25 |
| `machinery` | 1 | 1.6 | 1.0 | 0.9 | 1.1 | 1.15 |

---

## DMC-Boreal-SD-L

### DMC Boreal 矿石运输箱 L 型

> 粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Deepcore Mining Corporation  
**系列：** Boreal Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                     |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `template`          | 货柜结构ID       | `cargoverse:cargo/dmc/boreal/dmc_boreal_sd_l`                                                                                                                                                          |
| `display_name`      | 显示名称         | `DMC Boreal 矿石运输箱 L 型`                                                                                                                                                                                 |
| `cargo_description` | 货柜描述         | `§lDMC Boreal 矿石运输箱 L 型\n§r§7粗犷的耐磨框架能够承受原矿装载时的撞击和碎石摩擦，结构简单且便于矿区现场修补，是深岩矿业基层采掘作业的标准矿石箱。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：Boreal Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                  |
| `max_owned`         | 每个玩家的同时最大持有量 | 7                                                                                                                                                                                                      |
| `cargo_level`       | 货柜等级         | `L`                                                                                                                                                                                                    |
| `max_integrity`     | 最大完整性        | 130                                                                                                                                                                                                    |
| `blocked_affixes`   | 屏蔽词条         | 无                                                                                                                                                                                                      |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                      |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 13 × 7 × 7 |
| 体积 | 637 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 30 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `ore` | 5 | 1.9 | 1.25 | 1.25 | 1.2 | 1.3 |
| `stone` | 4 | 1.8 | 1.2 | 1.2 | 1.15 | 1.25 |
| `machinery` | 1 | 1.6 | 1.0 | 0.9 | 1.1 | 1.15 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
