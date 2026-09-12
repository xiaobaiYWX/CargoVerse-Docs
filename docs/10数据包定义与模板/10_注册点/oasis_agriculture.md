# 绿洲农业联盟注册点

[返回注册点目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:oasis_agriculture` |
| JSON 文件 | [oasis_agriculture.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/registration_point_definitions/oasis_agriculture.json>) |
| 终端翻牌名称 | 绿洲农业联盟 |
| 许可证类型 | 绿洲农业联盟合约特派员 |
| 初始许可证等级 | S |
| 基础货柜 | [VBS Harvest 农鲜周转柜 S 型](<../05_基础货柜/oasis_basic.md>) |
| 注册声望 | 50 |
| 投放状态 | 已绑定现有默认资源贸易点 |

## 物品奖励

| 物品 | 数量 |
| --- | --- |
| `minecraft:wheat_seeds` | 32 |

## 绑定与权益

贸易点的 `manufacturer` 应为 `cargoverse:vbs`，其 `modules.registration_point.definitions_pool` 引用本注册点定义。签发机构与注册声望归属来自承载贸易点的制造商。

基础货柜通过资产标记免调度点，满预算或超预算仍可领取；一次只允许一份基础货柜，重复注册不重复发放。注销仍按现有规则回收基础货柜，普通自有货柜保留。

## 当前 JSON

```json
{
  "schema_version": 1,
  "display_name": "绿洲农业联盟",
  "license_type": "绿洲农业联盟合约特派员",
  "initial_license_level": "S",
  "registration_rewards": {
    "starter_container": {
      "definition": "cargoverse:starter_containers/oasis_basic"
    },
    "items": [
      {
        "item": "minecraft:wheat_seeds",
        "count": 32
      }
    ]
  },
  "reputation_rewards": {
    "reputation_rewards": 50
  }
}
```
