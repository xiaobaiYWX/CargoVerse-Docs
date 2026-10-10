# 泉源净水所资源表

> **已接入（2026-10-07）：** 完整整站 NBT、贸易点定义、资源表、结构绑定与自然生成配置已发布；设备静态核对通过，地形、货柜装卸与营业流程仍待实机验收。

| 项目 | 设计内容 |
| --- | --- |
| 关联站点 | [G11 泉源净水所](<../../../07_贸易点/factory/泉源净水所/00_总体说明.md>) |
| 资源 ID | `cargoverse:factory/ground_station/spring_water_station` |
| 发布 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/factory/ground_station/spring_water_station.json` |
| schema_version | 2 |
| 引用方式 | 每行直接填写一个 CargoGood 完整 ID |
| 数量单位 | t 为数量符号；每日按 24000 ticks 计算 |
| 报价与库存 | 逐商品 price_multiplier；出售有限库存，收购无库存且全部设每日限额 |

## 出售 sales

全部使用有限 `inventory`；初始量、容量、日补分别对应 `initial`、`capacity`、`daily_restock`。当前均为持续补货，不增加一次性遗物来源。

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:general_supplies/potable_water_crates` | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 200 | 400 | 100 | 0.95 |
| `cargoverse:processed_resource/sorted_packaging_scrap` | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 20 | 40 | 10 | 0.5 |

## 收购 acquisitions

全部填写 `daily_limit`，额度由同一实例的所有玩家按每种货物共享，跨日恢复但不累计。不创建收购库存、不扣除材料来驱动出售。

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:machinery/industrial_pump_sets` | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | 5 | 1 |
| `cargoverse:chemical_material/sealing_resin` | [密封树脂](<../../../01_CargoGood/chemical_material/sealing_resin.md>) | 20 | 1 |
| `cargoverse:general_supplies/shelf_stable_rations` | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 60 | 1 |
| `cargoverse:energy_fuel/biomass_briquettes` | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | 60 | 1 |

## 数值依据

| 方向 | 货物 | 数量的业务依据 |
| --- | --- | --- |
| 出售 | [净水补给箱](<../../../01_CargoGood/general_supplies/potable_water_crates.md>) | 日常主货；容量可积存数柜，但单站日补低于大站集中供应 |
| 出售 | [分拣包装废料](<../../../01_CargoGood/processed_resource/sorted_packaging_scrap.md>) | 清洁包装与封装外箱，排除过滤污染物 |
| 收购 | [工业水泵机组](<../../../01_CargoGood/machinery/industrial_pump_sets.md>) | 少量设备更换，不是每日转化配方 |
| 收购 | [密封树脂](<../../../01_CargoGood/chemical_material/sealing_resin.md>) | 管路密封与箱体维护 |
| 收购 | [长效口粮](<../../../01_CargoGood/general_supplies/shelf_stable_rations.md>) | 常驻值守人员补给 |
| 收购 | [压制生物燃料](<../../../01_CargoGood/energy_fuel/biomass_briquettes.md>) | 小锅炉及值守取暖的低值燃料 |

普通来源初始两日量、容量四日量，让初见站点有可装运库存，持续补货仍受本站用途约束。生活和低价原料按整柜或数柜组织，专业设备使用小批替换额度，不为了装满 S 柜而夸大每日仪器需求。

数量与价格为待实机平衡设计。新增站点数量会叠加区域供给和共享额度，不以单站看似很小就忽略总量；结算取整、签约修正、防护损耗和实际航程仍需验证。

[站点总览](<../../../07_贸易点/factory/泉源净水所/00_总体说明.md>) · [资源表目录](<../../README.md>) · [贸易点目录](<../../../07_贸易点/README.md>)
