# 基础货柜制造台

> **历史示例：** 本定义已由 A／B 指令测试资源替换，不再作为当前发布配置。见[测试点入口](<../../../07_贸易点/market/测试贸易点A/00_总体说明.md>)。

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:resource/general/default` |
| JSON 文件 | `src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/resource/general/default.json` |
| Schema 版本 | 2 |
| 显示名称 | 基础货柜制造台 |
| 配方数量 | 1 |

## `atlas_sd_s`

| 货柜 | 最低繁荣 | 最低许可证 | 加工费 |
| --- | ---: | --- | ---: |
| `cargoverse:aui/atlas_sd_s` | 0 | S | 80 VB |

| 实体材料 | 数量 |
| --- | ---: |
| `minecraft:iron_ingot` | 16 |
| `minecraft:oak_planks` | 8 |
| `minecraft:glass` | 4 |
| `minecraft:redstone` | 2 |

这是当前唯一随模组发布的制造配方。Atlas L 与其他型号只有在完成各自实体物品配方后才加入定义，不使用旧抽象库存成本或空材料条目代替。

[返回货柜制造台定义设计](../../README.md)
