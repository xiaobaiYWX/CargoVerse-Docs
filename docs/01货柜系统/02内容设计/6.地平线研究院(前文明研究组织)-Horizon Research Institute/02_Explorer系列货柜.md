# Explorer 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列        | 规格    | 接口  | 定位    | 特点        |
| ----------- | ----- | --- | ----- | --------- |
| Explorer 系列 | S/M/L | SI  | 科考样本舱 | 野外采样；环境适应 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType | 中文名称 | 是否可用 | 适用规格 | CargoType 默认词条 ID | 简易描述 |
| --- | --- | :---: | --- | --- | --- |
| `agriculture` | 农业产品 | × | — | `time_limit` |  |
| `livestock` | 活体生物 | × | — | `height_limit` |  |
| `ore` | 矿石资源 | × | — | 无 |  |
| `wood` | 木材 | × | — | 无 |  |
| `stone` | 石材 | × | — | 无 |  |
| `fuel_resource` | 能源原料 | × | — | `flammable`<br>`radioactive`<br>`cold_proof` |  |
| `textile` | 纺织与轻工业品 | × | — | 无 |  |
| `security` | 安防与武装设备 | × | — | 无 |  |
| `component` | 工业零件 | × | — | `fragile` |  |
| `machinery` | 机械设备 | × | — | `keep_upright`<br>`fragile` |  |
| `electronics` | 电子设备 | √ | S/M/L | `moisture_proof`<br>`fragile` | 环境适应与模块化保存单元适合野外科考，可运输传感器、控制器和计算设备。 |
| `chemical` | 化工材料 | × | — | `radioactive` |  |
| `construction` | 建筑材料 | × | — | 无 |  |
| `structural_module` | 大型结构组件 | × | — | 无 |  |
| `supplies` | 生活补给 | √ | M/L | 无 | 环境适应与模块化保存单元适合野外科考，可运输食品、工具和聚落日常补给。 |
| `medical` | 医疗物资 | √ | S/M/L | `time_limit`<br>`cold_chain`<br>`light_sensitive` | 环境适应与模块化保存单元适合野外科考，可运输药品、医疗器械和急救物资。 |
| `luxury` | 贵重消费品 | × | — | `keep_upright`<br>`fragile` |  |
| `research_sample` | 科研样本 | √ | S/M/L | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` | 环境适应与模块化保存单元适合野外科考，可运输生物、地质和遗迹研究样本。 |
| `data` | 数据资源 | √ | S/M/L | `cold_proof`<br>`fragile`<br>`moisture_proof` | 环境适应与模块化保存单元适合野外科考，可运输数据服务器、存储阵列和加密资料。 |
| `experimental` | 实验品 | √ | M/L | 无 | 环境适应与模块化保存单元适合野外科考，可运输实验原型、未知装置和测试设备。 |

---

## HRI-Explorer-SI-S

### HRI Explorer 科考样本舱 S 型

> 通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。

**制造商：** Horizon Research Institute  
**系列：** Explorer Series  
**接口：** SI 滑轨接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                     |
| ------------------- | ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `template`          | 货柜结构ID       | `cargoverse:cargo/hri/explorer/hri_explorer_si_s`                                                                                                                                                      |
| `display_name`      | 显示名称         | `HRI Explorer 科考样本舱 S 型`                                                                                                                                                                               |
| `cargo_description` | 货柜描述         | `§lHRI Explorer 科考样本舱 S 型\n§r§7通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 S 型强调便携与快速交接，适合小批量货物及小型运输平台。\n§r§l制造商：Horizon Research Institute\n§r§l系列：Explorer Series\n§r§l接口：SI 滑轨接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                  |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                     |
| `cargo_level`       | 货柜等级         | `S`                                                                                                                                                                                                    |
| `max_integrity`     | 最大完整性        | 100                                                                                                                                                                                                    |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `light_sensitive`                                                                                                                                                                     |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                      |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 7 × 4 × 5 |
| 体积 | 140 |
| 质量占位方块数量 | 1 |
| 结构基本质量 | 16 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `electronics` | 2 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `medical` | 3 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `research_sample` | 5 | 1.1 | 1.55 | 0.6 | 1.55 | 1.6 |
| `data` | 3 | 1.1 | 1.45 | 0.65 | 1.5 | 1.5 |

---

## HRI-Explorer-SI-M

### HRI Explorer 科考样本舱 M 型

> 通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。

**制造商：** Horizon Research Institute  
**系列：** Explorer Series  
**接口：** SI 滑轨接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                          |
| ------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/hri/explorer/hri_explorer_si_m`                                                                                                                                                           |
| `display_name`      | 显示名称         | `HRI Explorer 科考样本舱 M 型`                                                                                                                                                                                    |
| `cargo_description` | 货柜描述         | `§lHRI Explorer 科考样本舱 M 型\n§r§7通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 M 型在容量、重量与周转效率之间取得平衡，是系列中的常用主力规格。\n§r§l制造商：Horizon Research Institute\n§r§l系列：Explorer Series\n§r§l接口：SI 滑轨接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                       |
| `max_owned`         | 每个玩家的同时最大持有量 | 10                                                                                                                                                                                                          |
| `cargo_level`       | 货柜等级         | `M`                                                                                                                                                                                                         |
| `max_integrity`     | 最大完整性        | 100                                                                                                                                                                                                         |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `light_sensitive`                                                                                                                                                                          |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                           |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 9 × 5 × 5 |
| 体积 | 225 |
| 质量占位方块数量 | 1 |
| 结构基本质量 | 25 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `electronics` | 2 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `supplies` | 2 | 1.1 | 1.0 | 1.0 | 1.1 | 1.2 |
| `medical` | 3 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `research_sample` | 5 | 1.1 | 1.55 | 0.6 | 1.55 | 1.6 |
| `data` | 3 | 1.1 | 1.45 | 0.65 | 1.5 | 1.5 |
| `experimental` | 4 | 1.1 | 1.6 | 0.55 | 1.65 | 1.6 |

---

## HRI-Explorer-SI-L

### HRI Explorer 科考样本舱 L 型

> 通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Horizon Research Institute  
**系列：** Explorer Series  
**接口：** SI 滑轨接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                         |
| ------------------- | ------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/hri/explorer/hri_explorer_si_l`                                                                                                                                                          |
| `display_name`      | 显示名称         | `HRI Explorer 科考样本舱 L 型`                                                                                                                                                                                   |
| `cargo_description` | 货柜描述         | `§lHRI Explorer 科考样本舱 L 型\n§r§7通过模块化保存单元和耐候外壳收纳土壤、矿物、生物样本及现场仪器，使地平线研究院的调查队能在复杂遗迹环境中完成采集与回运。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Horizon Research Institute\n§r§l系列：Explorer Series\n§r§l接口：SI 滑轨接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                      |
| `max_owned`         | 每个玩家的同时最大持有量 | 7                                                                                                                                                                                                          |
| `cargo_level`       | 货柜等级         | `L`                                                                                                                                                                                                        |
| `max_integrity`     | 最大完整性        | 100                                                                                                                                                                                                        |
| `blocked_affixes`   | 屏蔽词条         | `moisture_proof` `light_sensitive`                                                                                                                                                                         |
| `base_affixes`      | 货柜基础词条       | 无                                                                                                                                                                                                          |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 13 × 7 × 7 |
| 体积 | 637 |
| 质量占位方块数量 | 2 |
| 结构基本质量 | 108 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `electronics` | 2 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `supplies` | 2 | 1.1 | 1.0 | 1.0 | 1.1 | 1.2 |
| `medical` | 3 | 1.1 | 1.3 | 0.8 | 1.35 | 1.4 |
| `research_sample` | 5 | 1.1 | 1.55 | 0.6 | 1.55 | 1.6 |
| `data` | 3 | 1.1 | 1.45 | 0.65 | 1.5 | 1.5 |
| `experimental` | 4 | 1.1 | 1.6 | 0.55 | 1.65 | 1.6 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
