# Fortress 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列        | 规格    | 接口  | 定位     | 特点        |
| ----------- | ----- | --- | ------ | --------- |
| Fortress 系列 | XL | HD  | 堡垒部署模块 | 前线基地；大型装备 |

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
| `security` | 安防与武装设备 | √ | XL | 无 | 堡垒化结构可整体部署大型防务设施，可运输武器、装甲、雷达和安防设施。 |
| `component` | 工业零件 | × | — | `fragile` |  |
| `machinery` | 机械设备 | √ | XL | `keep_upright`<br>`fragile` | 堡垒化结构可整体部署大型防务设施，可运输机床、动力设备和工程机械。 |
| `electronics` | 电子设备 | × | — | `moisture_proof`<br>`fragile` |  |
| `chemical` | 化工材料 | × | — | `radioactive` |  |
| `construction` | 建筑材料 | √ | XL | 无 | 堡垒化结构可整体部署大型防务设施，可运输建材、管线和设施配套材料。 |
| `structural_module` | 大型结构组件 | √ | XL | 无 | 堡垒化结构可整体部署大型防务设施，可运输预制舱段、设备模块和大型结构件。 |
| `supplies` | 生活补给 | √ | XL | 无 | 堡垒化结构可整体部署大型防务设施，可运输食品、工具和聚落日常补给。 |
| `medical` | 医疗物资 | × | — | `time_limit`<br>`cold_chain`<br>`light_sensitive` |  |
| `luxury` | 贵重消费品 | × | — | `keep_upright`<br>`fragile` |  |
| `research_sample` | 科研样本 | × | — | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |  |
| `data` | 数据资源 | × | — | `cold_proof`<br>`fragile`<br>`moisture_proof` |  |
| `experimental` | 实验品 | × | — | 无 |  |

---

## BDS-Fortress-HD-XL

### BDS Fortress 堡垒部署模块 XL 型

> 将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。

**制造商：** Bastion Defense Systems  
**系列：** Fortress Series  
**接口：** HD 重型保持接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                  |
| ------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/bds/fortress/bds_fortress_hd_xl`                                                                                                                                                  |
| `display_name`      | 显示名称         | `BDS Fortress 堡垒部署模块 XL 型`                                                                                                                                                                          |
| `cargo_description` | 货柜描述         | `§lBDS Fortress 堡垒部署模块 XL 型\n§r§7将厚重装甲、大型防御装备、指挥设施和基础保障单元整合为可部署模块，用于在高风险区域快速建立长期前线基地。该 XL 型属于超规格平台，面向聚落级设施、战略物资和长期部署任务。\n§r§l制造商：Bastion Defense Systems\n§r§l系列：Fortress Series\n§r§l接口：HD 重型保持接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                               |
| `max_owned`         | 每个玩家的同时最大持有量 | 2                                                                                                                                                                                                   |
| `cargo_level`       | 货柜等级         | `XL`                                                                                                                                                                                                |
| `max_integrity`     | 最大完整性        | 170                                                                                                                                                                                                 |
| `blocked_affixes`   | 屏蔽词条         | `fragile` `radioactive`                                                                                                                                                                             |
| `base_affixes`      | 货柜基础词条       | `keep_upright`                                                                                                                                                                                      |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 16 × 16 × 16 |
| 体积 | 4096 |
| 质量占位方块数量 | 8 |
| 结构基本质量 | 12 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `security` | 5 | 2.5 | 1.65 | 0.45 | 1.75 | 1.7 |
| `machinery` | 4 | 2.4 | 1.5 | 0.55 | 1.6 | 1.6 |
| `construction` | 4 | 2.5 | 1.5 | 0.65 | 1.6 | 1.7 |
| `structural_module` | 5 | 2.5 | 1.7 | 0.4 | 1.8 | 1.8 |
| `supplies` | 3 | 2.4 | 1.5 | 0.55 | 1.6 | 1.6 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
