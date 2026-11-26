# 制造商注册点

当前提供八家制造商各一项注册点定义，初始许可证均为 S。成功注册仅赠对应制造商的一张已打印初始蓝图，不赠物资、货币或声望；制造仍需材料，初始货柜占用 0 调度点。

| 制造商全称 | 注册点定义 | 基础货柜 | 实际节点绑定 |
| --- | --- | --- | --- |
| 天穹联合工业 | [cargoverse:aui_industry](<aui_industry.md>) | [AUI Origin 启航货柜 S型](<../../02货柜/天穹联合工业/Origin 启航货柜/origin_s.md>) | 全部 AUI 空港贸易点 |
| 云港物流集团 | [cargoverse:spl_logistics](<spl_logistics.md>) | [SPL Parcel 轻邮货柜 S型](<../../02货柜/云港物流集团/Parcel 轻邮货柜/parcel_s.md>) | 全部 SPL 空港贸易点 |
| 深岩矿业集团 | [cargoverse:dmc_mining](<dmc_mining.md>) | [DMC Pitbox 矿勤货柜 S型](<../../02货柜/深岩矿业集团/Pitbox 矿勤货柜/pitbox_s.md>) | 全部 DMC 空港贸易点 |
| 绿洲农业联盟 | [cargoverse:oasis_agriculture](<oasis_agriculture.md>) | [VBS Seedbox 田园货柜 S型](<../../02货柜/绿洲农业联盟/Seedbox 田园货柜/seedbox_s.md>) | 全部 VBS 空港贸易点 |
| 赫利俄斯能源集团 | [cargoverse:hec_energy](<hec_energy.md>) | [HEC Ember 工勤货柜 S型](<../../02货柜/赫利俄斯能源集团/Ember 工勤货柜/ember_s.md>) | 全部 HEC 空港贸易点 |
| 地平线研究院 | [cargoverse:hri_research](<hri_research.md>) | [HRI Scout 勘察货柜 S型](<../../02货柜/地平线研究院/Scout 勘察货柜/scout_s.md>) | 全部 HRI 空港贸易点 |
| 铁壁防务集团 | [cargoverse:bds_defense](<bds_defense.md>) | [BDS Rampart 哨勤货柜 S型](<../../02货柜/铁壁防务集团/Rampart 哨勤货柜/rampart_s.md>) | 全部 BDS 空港贸易点 |
| 遗民贸易协会 | [cargoverse:rex_exchange](<rex_exchange.md>) | [REX Patchwork 拾荒货柜 S型](<../../02货柜/遗民贸易协会/Patchwork 拾荒货柜/patchwork_s.md>) | 全部 REX 空港贸易点 |

注册点定义本身不创建地图节点。所有具有制造商归属的正式空港贸易点都绑定该制造商唯一的注册点定义；地面小型贸易点不承载注册服务。签发制造商取自贸易点，所选注册点提供许可证类型和初始等级；签发制造商决定赠送的初始蓝图，货柜通过独立搭建器制造。

[初始货柜目录](<../../02货柜/初始货柜系列.md>) · [字段规则](<../../../04数据规范/贸易点/06_注册点与基础货柜定义.md>)
