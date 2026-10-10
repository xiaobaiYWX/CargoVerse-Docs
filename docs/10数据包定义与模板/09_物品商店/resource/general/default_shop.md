# 默认资源商店

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default_shop` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/shop_definitions/resource/general/default_shop.json` |
| Schema 版本 | 3 |
| 显示名称 | 默认资源商店 |
| 抽取次数 | 5 |
| 允许重复 | False |

## 商品

### `cargo_docking_connector`

| 权重 | 解锁繁荣 | 结果类型 | 物品 | 数量 | 基础价格 | 库存 |
| ---: | ---: | --- | --- | ---: | ---: | --- |
| 1 | 0 | `item` | `cargoverse:cargo_docking_connector` | 1 | 32 VB | 无限 |

### `iron_ingot_pack`

| 权重 | 解锁繁荣 | 结果类型 | 物品 | 数量 | 基础价格 | 库存 |
| ---: | ---: | --- | --- | ---: | ---: | --- |
| 1 | 0 | `item` | `minecraft:iron_ingot` | 3 | 64 VB | 每交易日 24 份 |

## 设计说明

- 对接器用于稳定供应，采用无限库存。
- 铁锭包采用有限库存；贸易点内所有售货机共享当日 24 份额度。
- 最终价格会应用购买玩家的制造商签约声望购买修正。
