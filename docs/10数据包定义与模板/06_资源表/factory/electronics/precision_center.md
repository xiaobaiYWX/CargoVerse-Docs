# 精密电子与测绘中心资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[H02 精密电子与测绘中心](<../../../07_贸易点/factory/electronics/精密电子与测绘中心.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:factory/electronics/precision_center` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/electronics/precision_center.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `communication_relays` | [通信中继器](<../../../01_CargoGood/electronics/communication_relays.md>) | `ingredient.electronics.communication_relays` | 2 | 6 | 2 | 常规周转 |
| `industrial_sensors` | [工业传感器](<../../../01_CargoGood/electronics/industrial_sensors.md>) | `ingredient.electronics.industrial_sensors` | 2 | 6 | 2 | 常规周转 |
| `data_storage_arrays` | [封装数据存储阵列](<../../../01_CargoGood/electronics/data_storage_arrays.md>) | `ingredient.electronics.data_storage_arrays` | 2 | 6 | 2 | 常规周转 |
| `high_purity_silicon_wafers` | [高纯硅片](<../../../01_CargoGood/refined_resource/high_purity_silicon_wafers.md>) | `ingredient.refined_resource.high_purity_silicon_wafers` | 2 | 6 | 2 | 常规周转 |
| `optical_glass_blanks` | [光学玻璃坯](<../../../01_CargoGood/refined_resource/optical_glass_blanks.md>) | `ingredient.refined_resource.optical_glass_blanks` | 4 | 12 | 4 | 常规周转 |
| `survey_drones` | [测绘无人机](<../../../01_CargoGood/vehicle/survey_drones.md>) | `ingredient.vehicle.survey_drones` | 1 | 3 | 1 | 常规周转 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `precision_copper_wire` | [精密铜线](<../../../01_CargoGood/refined_resource/precision_copper_wire.md>) | `ingredient.refined_resource.precision_copper_wire` | 0 | 10.5 | 3.5 | false | 常规周转 |
| `amethyst_resonator_plates` | [紫水晶谐振片](<../../../01_CargoGood/special_resource/amethyst_resonator_plates.md>) | `ingredient.special_resource.amethyst_resonator_plates` | 0 | 10.5 | 3.5 | false | 常规周转 |
| `nether_quartz_clusters` | [下界石英晶簇](<../../../01_CargoGood/special_resource/nether_quartz_clusters.md>) | `ingredient.special_resource.nether_quartz_clusters` | 0 | 10.5 | 3.5 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
