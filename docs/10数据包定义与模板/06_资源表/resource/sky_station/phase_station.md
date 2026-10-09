# 虚空相位研究站资源表

> **已接入 · 2026-10-06：** 本页为本站当前出售库存、日补、逐商品报价与每日收购限额的唯一维护表。关联站点：[H03 虚空相位研究站](<../../../07_贸易点/resource/虚空相位研究站/00_总体说明.md>)。新增目录仅自动用于新经济实例；已有实例保存资源目录快照。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/sky_station/phase_station` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/sky_station/phase_station.json` |
| schema_version | 1 |
| 匹配方式 | 每行独立规则；selector.match_mode 为 all；selector.tags 为该行唯一标签的单元素数组 |
| 数量单位 | t 是货物数量；完整贸易日为 24000 ticks |
| 报价方式 | 每条规则设置 price_multiplier；无站点总倍率 |

## 出售 sales

全部 create_inventory: true；初始量、容量、日补对应 initial_amount、capacity_per_good、daily_restock_per_good。价格倍率作用于基础价值，整笔结算后取整。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | ---: | ---: | ---: | ---: |
| `stabilized_ender_grains` | [稳相末影晶粒](<../../../01_CargoGood/special_resource/stabilized_ender_grains.md>) | `ingredient.special_resource.stabilized_ender_grains` | 200 | 400 | 100 | 0.95 |
| `contained_void_mixture` | [桶装虚空混合物](<../../../01_CargoGood/anomalous_cargo/contained_void_mixture.md>) | `ingredient.anomalous_cargo.contained_void_mixture` | 100 | 200 | 50 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 60 | 120 | 30 | 0.5 |
| `scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | `ingredient.mechanical_parts.scrapped_electronic_components` | 40 | 80 | 20 | 0.5 |

## 收购 acquisitions

收购不建库存。true 写入 daily_limit_enabled: true 与 daily_limit_per_good；false 不写限额字段，表示不限额。额度由同一站点实例所有玩家共享，按贸易日重置、不累积；price_multiplier 对该商品独立生效。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | ---: | ---: |
| `regenerative_culture_fluid` | [再生培养液](<../../../01_CargoGood/medical_supply/regenerative_culture_fluid.md>) | `ingredient.medical_supply.regenerative_culture_fluid` | true | 100 | 1.15 |
| `end_environment_samples` | [末地环境样本](<../../../01_CargoGood/research_sample/end_environment_samples.md>) | `ingredient.research_sample.end_environment_samples` | true | 100 | 1.15 |
| `data_storage_arrays` | [封装数据存储阵列](<../../../01_CargoGood/electronics/data_storage_arrays.md>) | `ingredient.electronics.data_storage_arrays` | false | 不限 | 1.1 |
| `memory_echo_media` | [记忆回声介质](<../../../01_CargoGood/anomalous_cargo/memory_echo_media.md>) | `ingredient.anomalous_cargo.memory_echo_media` | true | 5 | 1.2 |
| `non_euclidean_components` | [非欧几何构件](<../../../01_CargoGood/anomalous_cargo/non_euclidean_components.md>) | `ingredient.anomalous_cargo.non_euclidean_components` | true | 5 | 1.2 |
| `temporal_lag_clusters` | [时滞晶簇](<../../../01_CargoGood/anomalous_cargo/temporal_lag_clusters.md>) | `ingredient.anomalous_cargo.temporal_lag_clusters` | true | 5 | 1.2 |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | false | 不限 | 1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | false | 不限 | 1 |
| `first_aid_medicines` | [急救药剂](<../../../01_CargoGood/medical_supply/first_aid_medicines.md>) | `ingredient.medical_supply.first_aid_medicines` | false | 不限 | 1 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | false | 不限 | 1 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | false | 不限 | 1 |
| `industrial_energy_cells` | [工业蓄能电池](<../../../01_CargoGood/energy_fuel/industrial_energy_cells.md>) | `ingredient.energy_fuel.industrial_energy_cells` | true | 100 | 1.05 |
| `communication_relays` | [通信中继器](<../../../01_CargoGood/electronics/communication_relays.md>) | `ingredient.electronics.communication_relays` | true | 100 | 1.05 |
| `culture_medium` | [培养基原液](<../../../01_CargoGood/chemical_material/culture_medium.md>) | `ingredient.chemical_material.culture_medium` | false | 不限 | 1.05 |
| `industrial_sensors` | [工业传感器](<../../../01_CargoGood/electronics/industrial_sensors.md>) | `ingredient.electronics.industrial_sensors` | true | 100 | 1.05 |
| `precision_measuring_instruments` | [精密测量仪](<../../../01_CargoGood/tools_equipment/precision_measuring_instruments.md>) | `ingredient.tools_equipment.precision_measuring_instruments` | true | 100 | 1.05 |

## 业务用途与维护

异常研究专线核心，补齐常用生活和研究设备需求；桶装虚空混合物仍送 R03，稳相晶粒也可少量送 H01 作取样对照材料。普通包装和电子余料提供无需异常货柜的回程选择。

补货与收购独立运行，不依赖材料转化或邻站库存。5 / 5 / 0 的来源是每实例一次性批次，重复发现同型站会带来另一批库存；普通回收料不会刷新这些批次。

[本站网络职责与线路](<../../../07_贸易点/resource/虚空相位研究站/定义设计/02_贸易网络设计.md>) · [正式资源表目录](<../../README.md>) · [资源表目录](<../../README.md>)
