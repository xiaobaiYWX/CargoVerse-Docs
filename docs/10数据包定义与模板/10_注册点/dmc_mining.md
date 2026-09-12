# 深岩矿业集团注册点

[返回注册点目录](<README.md>)

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:dmc_mining` |
| JSON 文件 | [dmc_mining.json](<../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/registration_point_definitions/dmc_mining.json>) |
| 终端翻牌名称 | 深岩矿业集团 |
| 许可证类型 | 深岩矿业集团合约特派员 |
| 初始许可证等级 | S |
| 基础货柜 | [DMC Boreal 矿冶散料柜 M 型](<../05_基础货柜/dmc_basic.md>) |
| 注册声望 | 50 |
| 投放状态 | 注册点定义已提供，待同制造商贸易点绑定 |

## 物品奖励

无额外物品奖励。

## 绑定与权益

贸易点的 `manufacturer` 应为 `cargoverse:dmc`，其 `modules.registration_point.definitions_pool` 引用本注册点定义。签发机构与注册声望归属来自承载贸易点的制造商。

基础货柜通过资产标记免调度点，满预算或超预算仍可领取；一次只允许一份基础货柜，重复注册不重复发放。注销仍按现有规则回收基础货柜，普通自有货柜保留。

## 当前 JSON

```json
{
  "schema_version": 1,
  "display_name": "深岩矿业集团",
  "license_type": "深岩矿业集团合约特派员",
  "initial_license_level": "S",
  "registration_rewards": {
    "starter_container": {
      "definition": "cargoverse:starter_containers/dmc_basic"
    },
    "items": []
  },
  "reputation_rewards": {
    "reputation_rewards": 50
  }
}
```
