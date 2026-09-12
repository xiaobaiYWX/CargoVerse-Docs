# 默认农业资源表

## 基本信息

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/agriculture/default` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/resource_tables/resource/agriculture/default.json` |
| Schema 版本 | 1 |
| 用途 | 袋装小麦的独立出售资源表 |

## 出售规则

| 规则 ID | match_mode | 标签 | 创建库存 | 初始量 | 每种货物容量 | 每日补货 |
| --- | --- | --- | --- | ---: | ---: | ---: |
| `bagged_wheat` | `all` | `ingredient.agriculture.bagged_wheat` | 是 | 0t | 160t | 6t |

## 收购规则

无。
