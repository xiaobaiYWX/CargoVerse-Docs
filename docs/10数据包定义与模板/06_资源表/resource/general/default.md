# 默认资源贸易点资源表

> **历史示例：** 本定义已由 A／B 指令测试资源替换，不再作为当前发布配置。见[测试点入口](<../../../07_贸易点/market/测试贸易点A/00_总体说明.md>)。

## 基本信息

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/general/default.json` |
| Schema 版本 | 1 |
| 用途 | 默认资源贸易点的测试交易目录与库存周转 |

## 出售规则

| 规则 ID | match_mode | 标签 | 创建库存 | 初始量 | 每种货物容量 | 每日补货 |
| --- | --- | --- | --- | ---: | ---: | ---: |
| `hematite_ore` | `all` | `ingredient.raw_resource.hematite_ore` | 是 | 0t | 800t | 60t |
| `conifer_logs` | `all` | `ingredient.raw_resource.conifer_logs` | 是 | 0t | 800t | 30t |
| `greenhouse_fruit` | `all` | `ingredient.agriculture.greenhouse_fruit` | 是 | 0t | 800t | 60t |

## 收购规则

| 规则 ID | match_mode | 标签 |
| --- | --- | --- |
| `compound_fertilizer` | `all` | `ingredient.chemical_material.compound_fertilizer` |
| `biomass_briquettes` | `all` | `ingredient.energy_fuel.biomass_briquettes` |
