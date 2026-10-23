# 测试全型号货柜制造目录

更新：2026-10-23。A／B 指令测试站共用 `cargoverse:market/test_station/all_containers`，当前覆盖 **49 款：45 款固体、4 款液体**。两站同时提供以下四款液体柜，不参与商品买卖的 A／B 分组。

运行文件：[all_containers.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/trade_points/trade_points_subfunctions/cargo_manufacturing_platform_definitions/market/test_station/all_containers.json>)。完整配方见[制造配方与投放总表](<../../制造配方与投放总表.md>)；此处仅汇总液体测试范围。

| 制造商与系列 | 型号 | 定义 ID | 容量 | 空重 Kpg | 调度点 | 许可／最低繁荣度 |
| --- | --- | --- | ---: | ---: | ---: | --- |
| HRI Crucible 衬层液体罐柜 L 型 | L | `cargoverse:hri/crucible_si_l` | 240000 mB | 170 | 4 | L／2 |
| HRI Crucible 衬层液体罐柜 M 型 | M | `cargoverse:hri/crucible_si_m` | 120000 mB | 80 | 2 | M／1 |
| SPL Cistern 标准液体罐柜 L 型 | L | `cargoverse:spl/cistern_sd_l` | 240000 mB | 140 | 4 | L／2 |
| SPL Cistern 标准液体罐柜 M 型 | M | `cargoverse:spl/cistern_sd_m` | 120000 mB | 65 | 2 | M／1 |

当前 M 型测试配方为铁锭 32、橡木木板 16、玻璃 8、红石 4，加工费 160 VB；L 型为上述材料各两倍，加工费 320 VB。正常检查许可、材料、加工费和调度能力；测试站初始繁荣度 5 已满足两种配方门槛。

四款均使用同规格 AUI Atlas 占位结构，容量定义 1 对应 1000 mB。Crucible 当前没有已生效的衬层／耐腐蚀保护，不因系列名称自动具备能力。制造出的液体柜仅承载液体；“液体”不限制可配置的运输词条。

本目录已与源码及 build/resources/main 中的构建资源核对一致。尚未在本轮进入游戏进行制造操作；运行中的世界须使用最新资源后验证。自然站配方与气体／生物占位型号不因测试目录开放而自动投放。
