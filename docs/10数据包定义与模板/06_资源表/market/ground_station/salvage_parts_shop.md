# 旧件回收铺资源表

> **已接入（2026-10-07）：** 完整整站 NBT、贸易点定义、资源表、结构绑定与自然生成配置已发布；设备静态核对通过，地形、货柜装卸与营业流程仍待实机验收。

| 项目 | 设计内容 |
| --- | --- |
| 关联站点 | [G15 旧件回收铺](<../../../07_贸易点/market/旧件回收铺/00_总体说明.md>) |
| 资源 ID | `cargoverse:market/ground_station/salvage_parts_shop` |
| 发布 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/ground_station/salvage_parts_shop.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 为数量符号；每日按 24000 ticks 计算 |
| 报价与库存 | 逐商品 price_multiplier；出售有限库存，收购无库存且全部设每日限额 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补分别对应 `initial`、`capacity`、`daily_restock`。当前均为持续补货，不增加一次性遗物来源。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:mechanical_parts/standard_container_couplings` | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | 20 | 40 | 10 | 0.95 |
| `cargoverse:tools_equipment/mining_hand_tools` | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 30 | 60 | 15 | 0.95 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 20 | 40 | 10 | 0.5 |

## 收购 acquisitions

全部填写 `daily_limit`，额度由同一实例的所有玩家按每种货物共享，跨日恢复但不累计。不创建收购库存、不扣除材料来驱动出售。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:mechanical_parts/scrapped_electronic_components` | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | 40 | 1 |
| `cargoverse:processed_resource/recyclable_metal_scrap` | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 100 | 1 |
| `cargoverse:general_supplies/durable_workwear` | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 20 | 1 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 50 | 1 |
| `cargoverse:chemical_material/industrial_lubricant` | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 20 | 1 |

## 数值依据

| 方向 | 货物 | 数量的业务依据 |
| --- | --- | --- |
| 出售 | [标准货柜接口总成](<../../../01_CargoGood/mechanical_parts/standard_container_couplings.md>) | 检验合格的标准接口旧件，仅是抽象货物，不代表提供货柜制造 |
| 出售 | [矿务手工具](<../../../01_CargoGood/tools_equipment/mining_hand_tools.md>) | 整修后的小批通用工具，低于大型工具供应站规模 |
| 出售 | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 整修与分拣中产生的清洁包装 |
| 收购 | [报废电子组件](<../../../01_CargoGood/mechanical_parts/scrapped_electronic_components.md>) | 普通去电池电子件的地方接收额度 |
| 收购 | [可回收金属废料](<../../../01_CargoGood/processed_resource/recyclable_metal_scrap.md>) | 清洁金属回收主业务，限额避免取代大站批量处理 |
| 收购 | [耐用工装](<../../../01_CargoGood/general_supplies/durable_workwear.md>) | 分拣人员劳保 |
| 收购 | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 常驻人员补给 |
| 收购 | [工业润滑油](<../../../01_CargoGood/chemical_material/industrial_lubricant.md>) | 工具与旧件检验保养 |

普通来源初始两日量、容量四日量，让初见站点有可装运库存，持续补货仍受本站用途约束。生活和低价原料按整柜或数柜组织，专业设备使用小批替换额度，不为了装满 S 柜而夸大每日仪器需求。

数量与价格为待实机平衡设计。新增站点数量会叠加区域供给和共享额度，不以单站看似很小就忽略总量；结算取整、签约修正、防护损耗和实际航程仍需验证。

[站点总览](<../../../07_贸易点/market/旧件回收铺/00_总体说明.md>) · [资源表目录](<../../README.md>) · [贸易点目录](<../../../07_贸易点/README.md>)
