# 默认资源商店

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default_shop` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/shop_definitions/resource/general/default_shop.json` |
| Schema 版本 | 1 |
| 显示名称 | 默认资源商店 |
| 抽取次数 | 5 |
| 允许重复 | False |

## 商品

### `cargo_docking_connector`

| 权重 | 解锁繁荣 | 结果类型 | 物品 | 数量 | 价格 | 结算单位 |
| ---: | ---: | --- | --- | ---: | ---: | --- |
| 1 | 0 | `item` | `cargoverse:cargo_docking_connector` | 1 | 32 VB | `cargoverse:void_byte` |

| match_mode | output 标签 | 消耗量 |
| --- | --- | ---: |
| `any` | ingredient.mechanical_parts.standard_container_couplings | 1t |

### `iron_ingot_pack`

| 权重 | 解锁繁荣 | 结果类型 | 物品 | 数量 | 价格 | 结算单位 |
| ---: | ---: | --- | --- | ---: | ---: | --- |
| 1 | 0 | `item` | `minecraft:iron_ingot` | 3 | 64 VB | `cargoverse:void_byte` |

| match_mode | output 标签 | 消耗量 |
| --- | --- | ---: |
| `any` | ingredient.raw_resource.hematite_ore、ingredient.refined_resource.structural_steel_ingots | 1t |

## 设计说明

- （填写商品主题、抽取关系、价格和 output stock 消耗）
