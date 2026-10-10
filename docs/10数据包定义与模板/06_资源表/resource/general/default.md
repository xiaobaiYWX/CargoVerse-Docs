# 默认资源贸易点资源表

> **历史示例：** 本定义已由 A／B 指令测试资源替换，不再作为当前发布配置。见[测试点入口](<../../../07_贸易点/market/测试贸易点A/00_总体说明.md>)。

## 基本信息

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/general/default.json` |
| Schema 版本 | 2 |
| 用途 | 默认资源贸易点的测试交易目录与库存周转 |

## 出售规则

| CargoGood ID | 货物 | 初始量 | 容量 | 日补 | 价格倍率 |
| --- | --- | ---: | ---: | ---: | ---: |
| `cargoverse:raw_resource/hematite_ore` | — | 0t | 800t | 60t | 1 |
| `cargoverse:raw_resource/conifer_logs` | — | 0t | 800t | 30t | 1 |
| `cargoverse:agriculture/greenhouse_fruit` | — | 0t | 800t | 60t | 1 |

## 收购规则

| CargoGood ID | 货物 | 每日限额 | 价格倍率 |
| --- | --- | ---: | ---: |
| `cargoverse:chemical_material/compound_fertilizer` | — | 不限 | 1 |
| `cargoverse:energy_fuel/biomass_briquettes` | — | 不限 | 1 |
