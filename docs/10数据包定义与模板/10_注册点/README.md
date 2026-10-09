# 制造商注册点

当前提供八家制造商各一项注册点定义，初始许可证均为 S，首次注册声望为 50。基础货柜领取占用 0 调度点。

| 制造商全称 | 注册点定义 | 基础货柜 | 实际节点绑定 |
| --- | --- | --- | --- |
| 天穹联合工业 | [cargoverse:aui_industry](<aui_industry.md>) | [AUI Atlas 标准干货柜 S 型](<../05_基础货柜/aui_basic.md>) | 全部 AUI 空港贸易点 |
| 云港物流集团 | [cargoverse:spl_logistics](<spl_logistics.md>) | [SPL Courier 轻型配送柜 S 型](<../05_基础货柜/spl_basic.md>) | 全部 SPL 空港贸易点 |
| 深岩矿业集团 | [cargoverse:dmc_mining](<dmc_mining.md>) | [DMC Boreal 矿冶散料柜 M 型](<../05_基础货柜/dmc_basic.md>) | 全部 DMC 空港贸易点 |
| 绿洲农业联盟 | [cargoverse:oasis_agriculture](<oasis_agriculture.md>) | [VBS Harvest 农鲜周转柜 S 型](<../05_基础货柜/oasis_basic.md>) | 全部 VBS 空港贸易点及默认资源贸易点 |
| 赫利俄斯能源集团 | [cargoverse:hec_energy](<hec_energy.md>) | [HEC Apollo 燃料化工柜 S 型](<../05_基础货柜/hec_basic.md>) | 全部 HEC 空港贸易点 |
| 地平线研究院 | [cargoverse:hri_research](<hri_research.md>) | [HRI Explorer 科考样本舱 S 型](<../05_基础货柜/hri_basic.md>) | 全部 HRI 空港贸易点 |
| 铁壁防务集团 | [cargoverse:bds_defense](<bds_defense.md>) | [BDS Sentinel 安防装备柜 S 型](<../05_基础货柜/bds_basic.md>) | 全部 BDS 空港贸易点 |
| 遗民贸易协会 | [cargoverse:rex_exchange](<rex_exchange.md>) | [REX Salvage 旧世打捞柜 S 型](<../05_基础货柜/rex_basic.md>) | 全部 REX 空港贸易点 |

注册点定义本身不创建地图节点。所有具有制造商归属的正式空港贸易点都绑定该制造商唯一的注册点定义；地面小型贸易点不承载注册服务。签发制造商取自贸易点，所选注册点提供基础权益与许可证类型。

[基础货柜目录](<../05_基础货柜/README.md>) · [字段规则](<../../02贸易点系统/06_注册点与基础货柜定义.md>)
