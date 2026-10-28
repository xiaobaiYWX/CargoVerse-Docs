# 货柜现行目录

更新：2026-10-23。以运行 JSON 和实际 NBT 为准，不再维护已完成的模板制作计划。

> **本轮设计入口：** [固体货柜运输条件设计](<../../设计草案/待完成事项清单.md#固体货柜应用>)。本页保持当前实现；围护、食品时限、Eden／CryoVault 调整属于待实现目标。

## 当前规模与边界

- 本期 16 系列、45 个物品型号，全部使用最终确认的实际结构；Silo 最终为 L／X／XL，Apollo 为 M／L／X。
- 共 64 个主型号：45 款实装固体型号、6 款占位流体型号与 13 款后续专项。
- Silo 三款与 Reliquary 两款具有全型号测试站配方；正式站投放和最终材料平衡仍待专项确认，不把测试配方冒充正式设计。
- Cistern／Crucible 的 M／L 四款已开放基础液体业务与测试制造，暂用 AUI 同规格结构，M/L 暂定 120000/240000mB；Boreas M／L 也已接入统一液体业务与测试制造，其余 13 个专项型号不开放制造。
- [实际模板分配表](<模板重分配与搭建清单.md>)记录全部 45 款的规格、参数、结构和包络；[现行规则](<现行货柜规则.md>)说明承载、保护、初始权益与接口边界。

## 文档组织

按“制造商／系列／型号”查阅：制造商 README 为产品线索引，每个系列独立建目录，README 只写共有职责和规格索引，各型号独立页面维护定义、数值、兼容、结构、配方及当前 JSON。未实现的 5 系列／13 型号也在同一目录树中，以页首标记区分，不另堆一份集中型号正文。

模板分配与制造总表只作跨型号索引，不代替独立页面。

## 按职责选择系列

| 制造商／系列 | 职责和目标形态 | 当前生效保护 | 型号规格 | 当前阶段 |
| --- | --- | --- | --- | --- |
| [AUI Atlas 标准干货柜](<天穹联合工业/Atlas 标准干货柜/README.md>) | 独立固体 solid。 | 无专用保护 | S／M／L／X | 本期物品，可制造 |
| [AUI Hermes 轻量干货柜](<天穹联合工业/Hermes 轻量干货柜/README.md>) | 独立固体 solid。 | 无专用保护 | S／M／L | 本期物品，可制造 |
| [AUI Titan 重型框架柜](<天穹联合工业/Titan 重型框架柜/README.md>) | 独立固体 solid。 | 无专用保护 | L／X／XL | 本期物品，可制造 |
| [AUI Vulcan 精密固定柜](<天穹联合工业/Vulcan 精密固定柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D、定向固定 O | M／L／X | 本期物品，可制造 |
| [SPL Cistern 标准液体罐柜](<云港物流集团/Cistern 标准液体罐柜/README.md>) | liquid 液体。 | 无专用保护 | M／L | 基础液体已接入，AUI 占位结构 |
| [SPL Courier 轻型配送柜](<云港物流集团/Courier 轻型配送柜/README.md>) | 独立固体 solid。 | 防潮 D | S／M／L | 本期物品，可制造 |
| [SPL Express 防护快件舱](<云港物流集团/Express 防护快件舱/README.md>) | 独立固体 solid。 | 防震 V、防潮 D、定向固定 O | S | 本期物品，可制造 |
| [DMC Boreal 封闭散料柜](<深岩矿业集团/Boreal 封闭散料柜/README.md>) | 独立固体 solid。 | 无专用保护 | M／L／X／XL | 本期物品，可制造 |
| [DMC CoreVault 小批固体防护柜](<深岩矿业集团/CoreVault 小批固体防护柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D | S／M | 本期物品，可制造 |
| [DMC Silo 密闭粉料柜](<深岩矿业集团/Silo 密闭粉料柜/README.md>) | 独立固体 solid。 | 防潮 D | L／X／XL | 本期物品，可制造 |
| [VBS Aquarium 水生活物舱](<绿洲农业联盟/Aquarium 水生活物舱/README.md>) | living 活物（明确水生适配范围）。 | 无专用保护 | M／L | 后续专项，未制造 |
| [VBS BioPod 陆生活物舱](<绿洲农业联盟/BioPod 陆生活物舱/README.md>) | living 活物（明确陆生适配范围）。 | 无专用保护 | S／M／L | 后续专项，未制造 |
| [VBS Eden 大宗保鲜柜](<绿洲农业联盟/Eden 大宗保鲜柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D | X／XL | 后续专项，未制造 |
| [VBS Harvest 围护周转柜](<绿洲农业联盟/Harvest 围护周转柜/README.md>) | 独立固体 solid。 | 防潮 D | S／M／L | 本期物品，可制造 |
| [HEC Apollo 封装敏感品柜](<赫利俄斯能源集团/Apollo 封装敏感品柜/README.md>) | 独立固体 solid。 | 防潮 D、定向固定 O、易燃保护 I | M／L／X | 本期物品，可制造 |
| [HEC Boreas 压力气体柜](<赫利俄斯能源集团/Boreas 压力气体柜/README.md>) | liquid，适合易挥发流体。 | 气密 2 | M／L | 已接液体业务与测试制造，占位结构 |
| [HEC CryoVault 冷冻保存柜](<赫利俄斯能源集团/CryoVault 冷冻保存柜/README.md>) | 独立固体 solid。 | 防潮 D | S／M／L | 后续专项，未制造 |
| [HEC Reactor 屏蔽封装柜](<赫利俄斯能源集团/Reactor 屏蔽封装柜/README.md>) | 独立固体 solid。 | 防潮 D、定向固定 O | M／L／X | 需求确认后推进，未制造 |
| [HRI Crucible 衬层液体罐柜](<地平线研究院/Crucible 衬层液体罐柜/README.md>) | liquid 液体（明确衬层适配范围）。 | 无专用保护 | M／L | 基础液体已接入，AUI 占位结构 |
| [HRI Explorer 科考防护柜](<地平线研究院/Explorer 科考防护柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D、定向固定 O | S／M／L | 本期物品，可制造 |
| [BDS Fortress 超规格固定柜](<铁壁防务集团/Fortress 超规格固定柜/README.md>) | 独立固体 solid。 | 防震 V、定向固定 O | XL | 本期物品，可制造 |
| [BDS Sentinel 装备防护柜](<铁壁防务集团/Sentinel 装备防护柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D、定向固定 O | S／M／L／X | 本期物品，可制造 |
| [REX Reliquary 翻修封存柜](<遗民贸易协会/Reliquary 翻修封存柜/README.md>) | 独立固体 solid。 | 防震 V、防潮 D、定向固定 O | S／M | 本期物品，可制造 |
| [REX Salvage 翻修通用柜](<遗民贸易协会/Salvage 翻修通用柜/README.md>) | 独立固体 solid。 | 无专用保护 | S／M／L | 本期物品，可制造 |

## 模板状态与制作规则

[模板总清单](<模板重分配与搭建清单.md>) · [装载边界](<货物装载参考.md>) · [命名与品牌](<命名规则.md>) · [结构制作规范](<../../01货柜系统/01核心系统/10_货柜结构制作规范.md>)
