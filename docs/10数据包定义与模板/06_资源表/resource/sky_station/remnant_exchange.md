# 遗民打捞交换所资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[R01 遗民打捞交换所](<../../../07_贸易点/resource/遗民打捞交换所/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/sky_station/remnant_exchange` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/sky_station/remnant_exchange.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `old_world_alloy_fragments` | [旧世合金残片](<../../../01_CargoGood/special_resource/old_world_alloy_fragments.md>) | `ingredient.special_resource.old_world_alloy_fragments` | 5 | 5 | 0 | 0.95 |
| `memory_echo_media` | [记忆回声介质](<../../../01_CargoGood/anomalous_cargo/memory_echo_media.md>) | `ingredient.anomalous_cargo.memory_echo_media` | 5 | 5 | 0 | 0.95 |
| `precursor_navigation_cores` | [前文明导航核心](<../../../01_CargoGood/electronics/precursor_navigation_cores.md>) | `ingredient.electronics.precursor_navigation_cores` | 5 | 5 | 0 | 0.95 |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 100 | 200 | 50 | 0.95 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | 60 | 120 | 30 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 60 | 120 | 30 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `ruin_material_sections` | [遗迹材料切片](<../../../01_CargoGood/research_sample/ruin_material_sections.md>) | `ingredient.research_sample.ruin_material_sections` | false | 不限 | 1.15 |
| `field_sampling_kits` | [野外采样器](<../../../01_CargoGood/tools_equipment/field_sampling_kits.md>) | `ingredient.tools_equipment.field_sampling_kits` | false | 不限 | 1.1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | false | 不限 | 1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | false | 不限 | 1 |
| `mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | `ingredient.tools_equipment.mining_hand_tools` | false | 不限 | 1.05 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `communication_relays` | [通信中继器](<../../../01_CargoGood/electronics/communication_relays.md>) | `ingredient.electronics.communication_relays` | true | 100 | 1.05 |
| `scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | `ingredient.mechanical_parts.scrapped_electronic_components` | false | 不限 | 1 |

## 业务用途与维护

保留有限遗物主供与切片收购，兼售远征口粮、劳保，回收可拆用的普通电子组件；普通废料不会复制稀有遗物。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/resource/遗民打捞交换所/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
