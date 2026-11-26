# 深岩矿业集团注册点

[返回注册点目录](README.md)

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:dmc_mining` |
| JSON 文件 | [dmc_mining.json](<../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/registration_point_definitions/dmc_mining.json>) |
| 终端名称 | 深岩矿业集团 |
| 许可证类型 | 深岩矿业集团合约特派员 |
| 初始许可证等级 | S |
| 附赠蓝图 | DMC Pitbox 矿勤货柜 S型，`cargoverse:dmc/pitbox_s` |
| 其他注册奖励 | 无物资、货币或声望 |

## 绑定与获取

贸易点的 `manufacturer` 为 `cargoverse:dmc`，`modules.registration_point.definitions_pool` 引用本注册点。赠图依据制造商 `starter_container` 查找独立制造配方，不要求配方 ID 与货柜 ID 相同。

每次成功注册直接给予一张已打印蓝图，不消耗空白蓝图。背包满时掉落在玩家身边。已持有效许可证时重复点击不会赠图；注销后重新注册可以再次领取。初始型号不在任何打印目录中提供。

制造仍消耗铁锭16件、标准紧固件箱4件、工业构件箱2件。八家初始柜共享每人一个名额，在建、已建、失效或待删除资产均占位。注销不删除初始货柜；只有取消施工或实际删除资产才释放名额。型号与能力见[初始货柜系列](../../02货柜/初始货柜系列.md)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "display_name": "深岩矿业集团",
  "license_type": "深岩矿业集团合约特派员",
  "initial_license_level": "S"
}
```
