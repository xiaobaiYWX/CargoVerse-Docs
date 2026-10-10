# 特殊订单定义设计

本目录先以 Markdown 设计特殊订单的货柜、目的地、限制、难度与奖励，再同步到数据包 JSON。每个非唯一订单使用一份独立 Markdown 文件，目录层级复刻实际订单 ID。

数据包路径：

```text
data/<namespace>/trade_points/trade_points_subfunctions/special_order_definitions/<订单路径>.json
```

资源 ID 等于命名空间与相对文件路径。例如 `market/test_station/a_to_b.json` 对应 `cargoverse:market/test_station/a_to_b`。

## 空白设计模板

### 身份

| 项目 | 设计值 |
| --- | --- |
| 订单 ID | `namespace:path` |
| 显示名称 |  |
| 发布贸易点 |  |
| 内容定位 |  |

### SP 货柜

| 字段 | 设计值 | 说明 |
| --- | --- | --- |
| `template` |  | 结构模板完整 ID |
| `container_display_name` |  | 货柜显示名称 |
| `cargo_display_name` |  | 只供玩家识别的货物名称 |
| `cargo_class` |  | 贴花和分类使用的 CargoClass ID |
| `total_mass` |  | 整只 SP 货柜总质量 |
| `initial_integrity` |  | 初始货物完整度 |

特殊订单不填写容量、货物单位、空柜质量、调度点、特殊设计、设计缺陷或普通运输词条。

### 目的地

| 字段 | 设计值 |
| --- | --- |
| `trade_point_definitions` |  |
| `min_distance` |  |
| `max_distance` |  |

目的地列表填写贸易点定义 ID，不填写实例 UUID。运行时只从同维度、已登记、具有交付终端和特殊订单检查点的实际实例中选择。

### 难度

| 字段 | 设计值 |
| --- | ---: |
| `base` |  |
| `distance_per_1000_blocks` |  |

```text
最终难度 = base + 实际距离 / 1000 × distance_per_1000_blocks
         + 所有任务限制的 difficulty_bonus
```

### 任务限制

| 类型 | 难度加成 | 参数 | 设计值 |
| --- | ---: | --- | --- |
| `cargoverse:time_limit` |  | `base_ticks` |  |
|  |  | `ticks_per_1000_blocks` |  |
| `cargoverse:minimum_integrity` |  | `minimum` |  |
| `cargoverse:moisture_proof` |  | `damage_per_second` |  |
| `cargoverse:cold_proof` |  | `damage_per_second` |  |
| `cargoverse:keep_upright` |  | `damage_per_second`、`min_up_dot` |  |
| `cargoverse:fragile` |  | `speed_delta_threshold`、`damage_amount` |  |
| `cargoverse:cold_chain` |  | `damage_per_second` |  |
| `cargoverse:height_limit` |  | `height_threshold`、`damage_per_second` |  |
| `cargoverse:light_sensitive` |  | `light_threshold`、`damage_per_second` |  |
| `cargoverse:radioactive` |  | `radius`、`effect_ids`、`effect_duration_ticks`、`effect_amplifier` |  |
| `cargoverse:flammable` |  | `ignition_temperature`、日照／群系升降温参数、`burning_damage_per_second` |  |

删除不使用的行。没有 `time_limit` 即为不限时。每种类型最多一项，最多 16 项。所有参数必须写在 `parameters` 中，并为当前订单独立填写难度加成。特殊订单限制的完整参数和运行规则只以[任务限制、难度与奖励曲线](../../11特殊订单系统/02_任务限制难度与奖励曲线.md)为准。

### 基础奖励

| 字段 | 设计值 |
| --- | ---: |
| `void_bytes` |  |
| `license_experience` |  |
| `manufacturer_reputation` |  |

### 物品奖励

| 物品 ID | 基础数量 | 随难度缩放 |
| --- | ---: | --- |
|  |  | 是／否 |

最多 16 项；运行时结算单项数量限制为 1～2304。

### 奖励曲线

| 难度 | 奖励倍率 |
| ---: | ---: |
| 0 | 1.0 |

控制点之间线性插值，区间外使用最近端点倍率。数值奖励四舍五入，可缩放物品数量向下取整。

### 贸易点订单池绑定

订单不再通过外部订单池定义绑定。直接在发布贸易点定义的 `modules.special_orders` 中设计：

| 字段 | 设计值 |
| --- | --- |
| `offer_slots` | `1..5` |
| `orders[].order` | 本订单 ID |
| `orders[].min_prosperity_level` | 出现所需的最低贸易点繁荣等级 |
| `orders[].weight` | 正整数抽取权重 |

## 当前数据

- [测试贸易点 A → B](market/test_station/a_to_b.md)
- [测试贸易点 B → A](market/test_station/b_to_a.md)

字段层级、挂载方式和重载规则见[数据定义与维护](../../11特殊订单系统/04_数据定义与维护.md)，完整运行流程见[特殊订单系统](../../11特殊订单系统/README.md)。

[返回数据定义设计](../README.md)
