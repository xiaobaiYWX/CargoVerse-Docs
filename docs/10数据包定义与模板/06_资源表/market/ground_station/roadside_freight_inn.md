# 路畔货运驿站资源表

> **已接入（2026-10-07）：** 完整整站 NBT、贸易点定义、资源表、结构绑定与自然生成配置已发布；设备静态核对通过，地形、货柜装卸与营业流程仍待实机验收。

| 项目 | 设计内容 |
| --- | --- |
| 关联站点 | [G09 路畔货运驿站](<../../../07_贸易点/market/路畔货运驿站/00_总体说明.md>) |
| 资源 ID | `cargoverse:market/ground_station/roadside_freight_inn` |
| 发布 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/ground_station/roadside_freight_inn.json` |
| schema_version | 1 |
| 匹配方式 | 每行唯一 ingredient 标签，selector.match_mode 为 all |
| 数量单位 | t 为数量符号；每日按 24000 ticks 计算 |
| 报价与库存 | 逐商品 price_multiplier；出售有限库存，收购无库存且全部设每日限额 |

## 出售 sales

全部 `create_inventory: true`；初始量、容量、日补分别对应 initial_amount、capacity_per_good、daily_restock_per_good。当前均为持续补货，不增加一次性遗物来源。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | --- | --- | --- | --- | --- |
| `shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | `ingredient.general_supplies.shelf_stable_rations` | 160 | 320 | 80 | 0.95 |
| `civilian_lighting_kits` | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | `ingredient.general_supplies.civilian_lighting_kits` | 30 | 60 | 15 | 0.95 |
| `sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | `ingredient.processed_resource.sorted_packaging_scrap` | 40 | 80 | 20 | 0.5 |

## 收购 acquisitions

全部 `daily_limit_enabled: true`，额度由同一实例的所有玩家按每种货物共享，跨日恢复但不累计。不创建收购库存、不扣除材料来驱动出售。

| 规则 ID | 货物 | 标签 | 每日限额开关 | 每种货物每日上限（t） | 价格倍率 |
| --- | --- | --- | --- | --- | --- |
| `bagged_wheat` | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | `ingredient.agriculture.bagged_wheat` | true | 70 | 1 |
| `potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | `ingredient.general_supplies.potable_water_crates` | true | 100 | 1 |
| `kiln_dried_planks` | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | `ingredient.processed_resource.kiln_dried_planks` | true | 50 | 1 |
| `durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | `ingredient.general_supplies.durable_workwear` | true | 20 | 1 |

## 数值依据

| 方向 | 货物 | 数量的业务依据 |
| --- | --- | --- |
| 出售 | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 短途经销主货；日补约一至两柜，低于 S01 的主供量 |
| 出售 | [民用照明器具](<../../../01_CargoGood/general_supplies/civilian_lighting_kits.md>) | 仓棚及野外营地用灯具，不配置整套电子产品 |
| 出售 | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 拆包与旅舍仓储产生的清洁包装 |
| 收购 | [袋装麦粒](<../../../01_CargoGood/agriculture/bagged_wheat.md>) | 驿站厨房与附近旅客配给 |
| 收购 | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 住宿、厨房和日常饮水 |
| 收购 | [烘干木板](<../../../01_CargoGood/processed_resource/kiln_dried_planks.md>) | 货架、木箱与雨棚维修 |
| 收购 | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 驿站搬运人员换装 |

普通来源初始两日量、容量四日量，让初见站点有可装运库存，持续补货仍受本站用途约束。生活和低价原料按整柜或数柜组织，专业设备使用小批替换额度，不为了装满 S 柜而夸大每日仪器需求。

数量与价格为待实机平衡设计。新增站点数量会叠加区域供给和共享额度，不以单站看似很小就忽略总量；结算取整、签约修正、防护损耗和实际航程仍需验证。

[站点总览](<../../../07_贸易点/market/路畔货运驿站/00_总体说明.md>) · [资源表目录](<../../README.md>) · [贸易点目录](<../../../07_贸易点/README.md>)
