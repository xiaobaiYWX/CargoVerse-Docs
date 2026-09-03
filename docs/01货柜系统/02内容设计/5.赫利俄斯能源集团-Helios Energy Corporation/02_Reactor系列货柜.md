# Reactor 系列货柜设计

> 预留（内容设计）／待验收：保留世界观、命名、美术及历史平衡目标；已迁入数据包的型号以实际 cargo_containers 为准。下文旧整柜字段、类型表和数值不作为现行 JSON 契约，不能直接复制。
> 现行字段见[容器定义](<../../01核心系统/02_货柜定义系统.md>)与[货物定义](<../../01核心系统/05_货物类型.md>)；用[新设计模板](<../04_货柜设计模板.md>)继续制作。接口文字仅为展示／结构约定，不是容器数据字段。

| 产品系列       | 规格  | 接口  | 定位     | 特点       |
| ---------- | --- | --- | ------ | -------- |
| Reactor 系列 | L/X | HD  | 高能设备运输 | 厚重隔离；安全锁 |

## 适用货物

> 根据制造商业务范围和本系列产品定位预填；后续可在规格设计与数值平衡阶段进一步收窄。

> “CargoType 默认词条 ID”来自 `cargo_value_constants/default.json` 的 `cargo_type_affixes`，不在货柜定义中重复声明。
> `最终词条 = CargoType 默认词条 - 本规格 blocked_affixes`；`blocked_affixes` 是货柜根节点字段，对该规格的所有 CargoType 统一生效。

| CargoType | 中文名称 | 是否可用 | 适用规格 | CargoType 默认词条 ID | 简易描述 |
| --- | --- | :---: | --- | --- | --- |
| `agriculture`       | 农业产品    |  ×   | —    | `time_limit` |                                    |
| `livestock`         | 活体生物    |  ×   | —    | `height_limit` |                                    |
| `ore`               | 矿石资源    |  ×   | —    | 无 |                                    |
| `wood`              | 木材      |  ×   | —    | 无 |                                    |
| `stone`             | 石材      |  ×   | —    | 无 |                                    |
| `fuel_resource`     | 能源原料    |  √   | L/X  | `flammable`<br>`radioactive`<br>`cold_proof` | 厚重隔离与安全锁适合高能设备，可运输燃料、电池材料和高能介质。    |
| `textile`           | 纺织与轻工业品 |  ×   | —    | 无 |                                    |
| `security`          | 安防与武装设备 |  ×   | —    | 无 |                                    |
| `component`         | 工业零件    |  ×   | —    | `fragile` |                                    |
| `machinery`         | 机械设备    |  √   | L/X  | `keep_upright`<br>`fragile` | 厚重隔离与安全锁适合高能设备，可运输机床、动力设备和工程机械。    |
| `electronics`       | 电子设备    |  √   | L/X  | `moisture_proof`<br>`fragile` | 厚重隔离与安全锁适合高能设备，可运输传感器、控制器和计算设备。    |
| `chemical`          | 化工材料    |  ×   | —    | `radioactive` |                                    |
| `construction`      | 建筑材料    |  ×   | —    | 无 |                                    |
| `structural_module` | 大型结构组件  |  √   | X    | 无 | 厚重隔离与安全锁适合高能设备，可运输预制舱段、设备模块和大型结构件。 |
| `supplies`          | 生活补给    |  ×   | —    | 无 |                                    |
| `medical`           | 医疗物资    |  ×   | —    | `time_limit`<br>`cold_chain`<br>`light_sensitive` |                                    |
| `luxury`            | 贵重消费品   |  ×   | —    | `keep_upright`<br>`fragile` |                                    |
| `research_sample`   | 科研样本    |  ×   | —    | `time_limit`<br>`fragile`<br>`keep_upright`<br>`light_sensitive` |                                    |
| `data`              | 数据资源    |  ×   | —    | `cold_proof`<br>`fragile`<br>`moisture_proof` |                                    |
| `experimental`      | 实验品     |  √   | L/X  | 无 | 厚重隔离与安全锁适合高能设备，可运输实验原型、未知装置和测试设备。  |

---

## HEC-Reactor-HD-L

### HEC Reactor 高能设备运输 L 型

> 以厚重屏蔽层、多级安全锁和强化防护结构封装反应设备核心部件及高能装置，只允许在具备资质的设施之间进行受控运输。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。

**制造商：** Helios Energy Corporation  
**系列：** Reactor Series  
**接口：** HD 重型保持接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                    |
| ------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/hec/reactor/hec_reactor_hd_l`                                                                                                                                                       |
| `display_name`      | 显示名称         | `HEC Reactor 高能设备运输 L 型`                                                                                                                                                                              |
| `cargo_description` | 货柜描述         | `§lHEC Reactor 高能设备运输 L 型\n§r§7以厚重屏蔽层、多级安全锁和强化防护结构封装反应设备核心部件及高能装置，只允许在具备资质的设施之间进行受控运输。该 L 型扩大了承载空间并强化受力结构，面向批量货流和大型运输平台。\n§r§l制造商：Helios Energy Corporation\n§r§l系列：Reactor Series\n§r§l接口：HD 重型保持接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                 |
| `max_owned`         | 每个玩家的同时最大持有量 | 7                                                                                                                                                                                                     |
| `cargo_level`       | 货柜等级         | `L`                                                                                                                                                                                                   |
| `max_integrity`     | 最大完整性        | 155                                                                                                                                                                                                   |
| `blocked_affixes`   | 屏蔽词条         | `radioactive` `flammable`                                                                                                                                                                             |
| `base_affixes`      | 货柜基础词条       | `cold_proof`                                                                                                                                                                                          |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 13 × 7 × 8 |
| 体积 | 728 |
| 质量占位方块数量 | 4 |
| 结构基本质量 | 4 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `fuel_resource` | 4 | 2.4 | 1.6 | 0.55 | 1.7 | 1.5 |
| `machinery` | 4 | 2.2 | 1.5 | 0.6 | 1.6 | 1.4 |
| `electronics` | 2 | 2.2 | 1.4 | 0.5 | 1.6 | 1.4 |
| `experimental` | 4 | 2.3 | 1.8 | 0.4 | 1.8 | 1.6 |

---

## HEC-Reactor-HD-X

### HEC Reactor 高能设备运输 X 型

> 以厚重屏蔽层、多级安全锁和强化防护结构封装反应设备核心部件及高能装置，只允许在具备资质的设施之间进行受控运输。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。

**制造商：** Helios Energy Corporation  
**系列：** Reactor Series  
**接口：** HD 重型保持接口

### 货柜预览截图

【待添加】

### 货柜基础参数

| 参数                  | 名称           | 内容                                                                                                                                                                                                        |
| ------------------- | ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `template`          | 货柜结构ID       | `cargoverse:cargo/hec/reactor/hec_reactor_hd_x`                                                                                                                                                           |
| `display_name`      | 显示名称         | `HEC Reactor 高能设备运输 X 型`                                                                                                                                                                                  |
| `cargo_description` | 货柜描述         | `§lHEC Reactor 高能设备运输 X 型\n§r§7以厚重屏蔽层、多级安全锁和强化防护结构封装反应设备核心部件及高能装置，只允许在具备资质的设施之间进行受控运输。该 X 型服务于大型工程与长距离主干运输，可容纳更完整的设备或更大批量货物。\n§r§l制造商：Helios Energy Corporation\n§r§l系列：Reactor Series\n§r§l接口：HD 重型保持接口` |
| `currency_id`       | 交易物品ID       | `cargoverse:enderite`                                                                                                                                                                                     |
| `max_owned`         | 每个玩家的同时最大持有量 | 5                                                                                                                                                                                                         |
| `cargo_level`       | 货柜等级         | `X`                                                                                                                                                                                                       |
| `max_integrity`     | 最大完整性        | 155                                                                                                                                                                                                       |
| `blocked_affixes`   | 屏蔽词条         | `radioactive` `flammable`                                                                                                                                                                                 |
| `base_affixes`      | 货柜基础词条       | `cold_proof`                                                                                                                                                                                              |

### 结构信息

| 项目 | 内容 |
| --- | --- |
| 模板尺寸 | 16 × 10 × 9 |
| 体积 | 1440 |
| 质量占位方块数量 | 4 |
| 结构基本质量 | 4 |

### CargoType 参数

> 修正倍率不填写时默认为 `1.0`；`weight` 越高越容易被抽取。实际货柜 JSON 只填写 `weight` 与可选的五项微调倍率；初始词条来自 `cargo_type_affixes`，再由根节点 `blocked_affixes` 统一屏蔽。

| `cargo_type` | `weight` | `mass_modifier` | `price_modifier` | `cargo_units_modifier` | `license_modifier` | `prosperity_modifier` |
| --- | :---: | :---: | :---: | :---: | :---: | :---: |
| `fuel_resource` | 4 | 2.4 | 1.6 | 0.55 | 1.7 | 1.5 |
| `machinery` | 4 | 2.2 | 1.5 | 0.6 | 1.6 | 1.4 |
| `electronics` | 2 | 2.2 | 1.4 | 0.5 | 1.6 | 1.4 |
| `structural_module` | 4 | 2.5 | 1.6 | 0.5 | 1.7 | 1.55 |
| `experimental` | 4 | 2.3 | 1.8 | 0.4 | 1.8 | 1.6 |

[返回制造商目录](README.md)  
[返回货柜内容设计](../README.md)
