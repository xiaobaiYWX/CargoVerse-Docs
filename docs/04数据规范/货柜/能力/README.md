# 货柜能力

能力写在货柜定义的 `abilities`，决定货柜的防护和设备。参数见逐项页面。

| 能力 | ID | 影响的核心数值 |
| --- | --- | --- |
| [围护等级](01_围护等级.md) | `cargoverse:containment` | 粉料散失 |
| [密封等级](02_密封等级.md) | `cargoverse:sealing` | 易挥发损失及液体舱准入 |
| [气压调节](03_压力调节.md) | `cargoverse:pressure_control` | 气压敏感 |
| [防水柜体](04_湿度控制.md) | `cargoverse:waterproof_body` | 降雨与浸水 |
| [缓冲衬垫](05_缓冲衬垫.md) | `cargoverse:cushioning` | [速度变化](<../../../02系统规则/运输状态/07_速度变化.md>) |
| [朝向保持](06_朝向保持.md) | `cargoverse:orientation_control` | [内部承载面倾角](<../../../02系统规则/运输状态/08_内部承载面倾角.md>) |
| [真空隔层](07_真空隔层.md) | `cargoverse:vacuum_insulation` | 高温和低温敏感 |
| [主动调温](08_主动调温.md) | `cargoverse:thermal_control` | 冷冻和保温运输暴露防护 |
| [遮光结构](09_遮光结构.md) | `cargoverse:light_blocking` | [内部光照](<../../../02系统规则/运输状态/06_内部光照.md>) |
| [内部照明](10_内部照明.md) | `cargoverse:internal_lighting` | [内部光照](<../../../02系统规则/运输状态/06_内部光照.md>) |

能力使用实际配置。气压调节、真空隔层和主动调温的可选等级用于图标和名称。防水柜体只需配置空对象。

[货物条件](<../../运输属性/运输条件/README.md>) · [核心数值](<../../../02系统规则/运输状态/README.md>) · [共用配置协议](<../../运输属性/00_配置公共协议.md>) · [货柜系统](<../../../02系统规则/货物与货柜/README.md>)
