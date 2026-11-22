# 货物运输条件

逐物品、逐流体或逐生物的 `transport_conditions` 声明货物的运输要求。玩家可以按要求规划路线，或选择有对应保护能力的货柜。

| 条件 | ID | 触发条件 | 对应能力 |
| --- | --- | --- | --- |
| [易碎品](01_易碎品.md) | `cargoverse:fragile` | 相邻速度采样差超过耐受 | 缓冲衬垫 |
| [保持正放](02_保持正放.md) | `cargoverse:keep_upright` | 承载面倾角超过上限 | 朝向保持 |
| [保持干燥](03_保持干燥.md) | `cargoverse:keep_dry` | 货柜所在地降雨或柜体浸水 | 防水柜体 |
| [保温运输](04_易腐坏.md) | `cargoverse:warm_transport` | 持续缺少主动调温时产生货损 | 主动调温 |
| [冷冻运输](05_冷冻运输.md) | `cargoverse:frozen_transport` | 持续缺少主动调温时产生货损 | 主动调温 |
| [低温敏感](06_低温敏感.md) | `cargoverse:cold_sensitive` | 群系气候低于下限 | 真空隔层 |
| [高温敏感](07_高温敏感.md) | `cargoverse:heat_sensitive` | 群系气候高于上限 | 真空隔层 |
| [避光储存](08_避光储存.md) | `cargoverse:light_sensitive` | 有效光照高于上限 | 遮光结构 |
| [保持光照](09_保持光照.md) | `cargoverse:requires_light` | 有效光照低于下限 | 内部照明 |
| [气压敏感](10_气压敏感.md) | `cargoverse:pressure_sensitive` | 世界高度超出允许范围 | 气压调节 |
| [粉料](12_粉料.md) | `cargoverse:powder` | 缺少围护，随时间散失 | 围护等级 1 |
| [易挥发](13_易挥发.md) | `cargoverse:volatile` | 缺少密封，随时间散失 | 密封等级 1 |

[货柜能力](<../../货柜/能力/README.md>) · [运行时](<../../../02系统规则/货物与货柜/14_运输数值运行时.md>)
