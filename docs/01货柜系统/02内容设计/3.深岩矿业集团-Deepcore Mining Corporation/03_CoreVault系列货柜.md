# CoreVault 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列         | 规格  | 接口  | 定位     | 特点         |
| ------------ | --- | --- | ------ | ---------- |
| CoreVault 系列 | S/M | SD  | 稀有矿物存储 | 高价值矿物；防护强化 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType           | 中文名称    | 是否可用 | 适用规格 | CargoType 默认词条 ID                                                | 简易描述                               |
| ------------------- | ------- | :--: | ---- | ---------------------------------------------------------------- | ---------------------------------- |
| `agriculture`       | 农业产品    |  ×   | —    | `time_limit`                                                     |                                    |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit`                                                   |                                    |
| `ore`               | 矿石资源    |  √   | S/M  | 无                                                                | 强化防护和分隔内仓适合高价值矿物，可运输原矿、精炼矿料和稀有矿石。  |
| `wood`              | 木材      |  ×   | —    | 无                                                                |                                    |
| `stone`             | 石材      |  ×   | —    | 无                                                                |                                    |
| `fuel_resource`     | 能源原料    |  ×   | —    | `flammable`<br>`radioactive`<br>`cold_proof`                     |                                    |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无                                                                |                                    |
| `security`          | 安防与武装设备 |  ×   | —    | 无                                                                |                                    |
| `component`         | 工业零件    |  ×   | —    | `fragile`                                                        |                                    |
| `machinery`         | 机械设备    |  ×   | —    | `keep_upright`<br>`fragile`                                      |                                    |
| `electronics`       | 电子设备    |  ×   | —    | `moisture_proof`<br>`fragile`                                    |                                    |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive`                                                    |                                    |
| `construction`      | 建筑材料    |  ×   | —    | 无                                                                |                                    |
| `structural_module` | 大型结构组件  |  ×   | —    | 无                                                                |                                    |
| `supplies`          | 生活补给    |  ×   | —    | 无                                                                |                                    |
| `medical`           | 医疗物资    |  ×   | —    | `time_limit`<br>`cold_chain`<br>`light_sensitive`                |                                    |
| `luxury`            | 贵重消费品   |  √   | S/M  | `keep_upright`<br>`fragile`                                      | 强化防护和分隔内仓适合高价值矿物，可运输珠宝、艺术品和高价值消费品。 |
| `research_sample`   | 科研样本    |  √   | S/M  | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` | 强化防护和分隔内仓适合高价值矿物，可运输生物、地质和遗迹研究样本。  |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof`                    |                                    |
| `experimental`      | 实验品     |  √   | S/M  | 无                                                                | 强化防护和分隔内仓适合高价值矿物，可运输原型设备。          |

---

## DMC-CoreVault-SD-S

### DMC CoreVault 稀有矿物存储 S 型

> 通过装甲外壳、缓冲内衬与分隔式内仓保护宝石、稀有晶体及高纯矿物，并以独立封条满足矿区和交易点之间的安全交接。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。

**制造商：** Deepcore Mining Corporation  
**系列：** CoreVault Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                     |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `template`          | 货柜结构ID       | `cargoverse:cargo/dmc/corevault/dmc_corevault_sd_s`                                                                                                                                                    |
| `display_name`      | 显示名称         | `DMC CoreVault 稀有矿物存储 S 型`                                                                                                                                                                             |
| `cargo_description` | 货柜描述         | `§lDMC CoreVault 稀有矿物存储 S 型\n§r§7通过装甲外壳、缓冲内衬与分隔式内仓保护宝石、稀有晶体及高纯矿物，并以独立封条满足矿区和交易点之间的安全交接。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：CoreVault Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                  |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                     |
| `cargo_level`       | 货柜等级         | `S`                                                                                                                                                                                                    |
| `max_integrity`     | 最大完整性        | 140                                                                                                                                                                                                    |
| `blocked_affixes`   | 屏蔽词条         | `fragile` `keep_upright`  `moisture_proof`  `radioactive`                                                                                                                                              |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                      |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 6 × 4 × 6 |
| 体积 | 144 |
| 质量占位方块数量 | 4 |
| 结构基本质量 | 4 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `ore` | 5 | 1.8 | 1.55 | 0.75 | 1.4 | 1.35 |
| `luxury` | 5 | 1.8 | 1.65 | 0.55 | 1.5 | 1.3 |
| `research_sample` | 3 | 1.8 | 1.5 | 0.55 | 1.45 | 1.35 |
| `experimental` | 2 | 1.8 | 1.6 | 0.45 | 1.55 | 1.4 |

---

## DMC-CoreVault-SD-M

### DMC CoreVault 稀有矿物存储 M 型

> 通过装甲外壳、缓冲内衬与分隔式内仓保护宝石、稀有晶体及高纯矿物，并以独立封条满足矿区和交易点之间的安全交接。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Deepcore Mining Corporation  
**系列：** CoreVault Series  
**接口：** SD 标准对接接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                          |
| ------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/dmc/corevault/dmc_corevault_sd_m`                                                                                                                                                         |
| `display_name`      | 显示名称         | `DMC CoreVault 稀有矿物存储 M 型`                                                                                                                                                                                  |
| `cargo_description` | 货柜描述         | `§lDMC CoreVault 稀有矿物存储 M 型\n§r§7通过装甲外壳、缓冲内衬与分隔式内仓保护宝石、稀有晶体及高纯矿物，并以独立封条满足矿区和交易点之间的安全交接。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Deepcore Mining Corporation\n§r§l系列：CoreVault Series\n§r§l接口：SD 标准对接接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                       |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                          |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                                         |
| `max_integrity`     | 最大完整性        | 140                                                                                                                                                                                                         |
| `blocked_affixes`   | 屏蔽词条         | `fragile` `keep_upright`  `moisture_proof`  `radioactive`                                                                                                                                                   |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                           |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 8 × 5 × 7 |
| 体积 | 280 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 4 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `ore` | 5 | 1.8 | 1.55 | 0.75 | 1.4 | 1.35 |
| `luxury` | 5 | 1.8 | 1.65 | 0.55 | 1.5 | 1.3 |
| `research_sample` | 3 | 1.8 | 1.5 | 0.55 | 1.45 | 1.35 |
| `experimental` | 2 | 1.8 | 1.6 | 0.45 | 1.55 | 1.4 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
