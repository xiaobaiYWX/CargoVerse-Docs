# 旧世珍品商馆资源表

> 已同步内置数据包；自然结构待补。关联贸易点：[R02 旧世珍品商馆](<../../../07_贸易点/market/valuables/旧世珍品商馆.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:market/valuables/heritage_gallery` |
| 目标 JSON | `src/main/resources/data/cargoverse/trade_points/resource_tables/market/valuables/heritage_gallery.json` |
| schema_version | 1 |
| 规则约定 | 每行独立规则；`selector.match_mode: all`；`selector.tags` 为该行标签组成的单元素数组；`create_inventory: true` |
| 数量单位 | t，每种货物独享容量；自然变化按完整贸易日结算 |

## 出售 sales

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日补对应 `daily_restock_per_good`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日补 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| `aged_spirits` | [陈酿佳酿](<../../../01_CargoGood/valuables/aged_spirits.md>) | `ingredient.valuables.aged_spirits` | 4 | 12 | 4 | 常规周转 |
| `artisan_jewelry` | [精工饰品](<../../../01_CargoGood/valuables/artisan_jewelry.md>) | `ingredient.valuables.artisan_jewelry` | 1 | 3 | 1 | 常规周转 |
| `restored_old_world_art` | [修复旧世艺术品](<../../../01_CargoGood/valuables/restored_old_world_art.md>) | `ingredient.valuables.restored_old_world_art` | 1 | 1 | 0 | 有限批次 |

## 收购 acquisitions

初始量对应 `initial_amount`，容量对应 `capacity_per_good`，日耗对应 `daily_consumption_per_good`，满库策略对应 `accept_when_full`。

| 规则 ID | 货物 | 标签 | 初始量 | 容量 | 日耗 | 满库继续收购 | 库存定位 |
| --- | --- | --- | ---: | ---: | ---: | --- | --- |
| `cut_gemstones` | [切磨宝石](<../../../01_CargoGood/valuables/cut_gemstones.md>) | `ingredient.valuables.cut_gemstones` | 0 | 9 | 3 | false | 常规周转 |

## 设计说明

收购代表本地或企业网络需求；出售由站外供给维持。任意收购货物断供不影响出售补货。首版全部使用有库存条目，满库停止收购。

有限批次日补／日耗为 0。售出后本实例不会自动恢复；买方容量为独立验收额度，接满后不再收购。自然变化不表示运输耗时、加工时间或生产效率。

[贸易网络总览](<../../../07_贸易点/设计总览.md>) · [100 项货物覆盖](<../../../07_贸易点/供需覆盖与数值校核.md>) · [资源表目录](<../../README.md>)

## 生成密度口径

本资源表收购日耗已按[自然生成密度设计基准](<../../../07_贸易点/生成密度与库存校核.md>)调整，不再假定每种贸易点各有一个实例。出售数量保持原设计，收购日耗按相对预期密度折算并向上取整到 0.25 t；常规收购容量为三日日耗且至少 3 t。有限批次仍为容量 1 t、日耗 0。这里保存的是明确数值，运行时不动态计算生成概率。
