# 实际物品基础属性与运输条件

> 当前正在进行数值运输第三轮数据／显示切换：下列 schema 1 是仍在内置资源中使用的定义资料，其 transport_requirements 不再执行旧行为。新数值数据使用 schema 2 的 transport，示例与当前边界见[运输数值运行时](../../01货柜系统/01核心系统/14_运输数值运行时.md)。不要将旧参数当作目前实际扣量依据。

每个物品一份 schema 1 属性文件；不使用条件集、成员标签或共享 profile。四种源码形态为 solid 独立固体、liquid 液体、gas 气体、living 活体。当前实际物品闭环只开放 solid；其余形态不代表液体、气体或活体载荷已经实现。颗粒和粉末物品也属于 solid。

## 目录与身份

目录为 `data/<物品命名空间>/cargoverse_item_properties/<形态>/<物品路径>.json`。例如：

- `data/minecraft/cargoverse_item_properties/solid/cake.json` → `minecraft:cake`。
- `data/create/cargoverse_item_properties/solid/shaft.json` → `create:shaft`。

文件内 form 必须与目录一致；物品 ID 从命名空间和路径推导，不重复填写。不同形态目录重复声明同一物品时整代拒绝发布，不能靠文件顺序覆盖。同一路径的数据包覆盖遵循原版资源包优先级。未知物品、空气、错误参数、不存在／不是静态贴花的方块引用以及模板占位贴花引用均拒绝。

## 文件示例

以下是蛋糕当前基础属性；本轮保留已有运输参数，不擅自增加保鲜时间或未完成的冷链行为。

```json
{
  "schema_version": 1,
  "form": "solid",
  "unit_mass": 0.1,
  "decal": "cargoverse:decal_food",
  "admission_policy": "standard",
  "transport_requirements": []
}
```

| 字段 | 含义 |
| --- | --- |
| schema_version | 当前为 1 |
| form | solid／liquid／gas／living，必须与目录一致 |
| unit_mass | 单件运输质量 Kpg；内置用 0～1 的整数或一位小数，零质量仍占容量 |
| decal | 已注册静态贴花方块 ID，例如 cargoverse:decal_food，不再由形态推导 |
| admission_policy | standard／empty_storage／blocked，独立于形态与保护 |
| transport_requirements | 直接写本物品的条件与参数数组；空数组表示无额外条件 |

条件行为仍由程序实现，数据包选择行为并填写参数；不接受条件集引用、价格、经验、完整度或容量权重。现有 V／D／O／I 参数保持不变；保鲜、温控等条件需专项确认后再配置。

## 缺失配置与安全边界

缺失文件时使用源码默认：solid、0.1 Kpg、standard、无额外条件、cargoverse:decal_none。没有默认 JSON，也不按名称、配方或用途猜测属性。未知私有容器仍需通过通用组件／库存安全检查，默认值不能绕过准入。

empty_storage 只能调用已审阅的真实验空适配；`data/cargoverse/item_storage_adapters.json` 只维护可验证的适配 ID，不保存质量、形态或条件，不能通过单改物品声明添加未知适配器。

## 装载、贴花与同步

一柜一种实际物品及完整组件状态；1 个物品占 1 容量单位。允许形态决定基本承载，缺少保护则提示风险，不恢复粉末／颗粒白名单。容器中的流体、实体和嵌套库存不因属于 solid 自动获准。

装载时冻结质量、条件、准入与声明贴花，运输快照 schema 为 3；卸空后贴花归 none。重载只影响下一次装载，不改写途中货物；贴花变化也视为规则变化，不能追加到不同快照。货柜实体和型号预览使用冻结贴花，警示贴花仍按实际剩余风险显示。

物品栏悬停不显示四大形态或默认分类来源。佩戴护目镜时，blocked 只显示“无法装载”，empty_storage 显示“仅允许空容器”，已有需求只显示“运输需求：词条名称”；普通无需求物品不添加运输提示行。

客户端元数据仍包含形态、准入与风险位，供既有界面筛选等使用；隐藏提示不删除底层属性或改变装载规则。目录在登录／reload 分包同步，不发送整份属性文件或新增逐物品请求；物理贴花通过原有方块状态更新同步。协议为 69。

## 维护与验证

2312 份文件覆盖现有所有非空气注册物品，六个来源命名空间；本轮质量、准入及已生效损耗参数保持不变。JSON 是唯一维护源，分类清单为查阅投影。微调一个物品直接修改对应文件；不要从 Markdown 重新生成并覆盖属性。

运行 `node tools/verify-item-properties.cjs` 作只读检查，再按影响范围选择运输、准入、快照及真实资源注册测试。自然站价格和收购经验仍在报价中维护；液体、生物闭环以及冷链能耗不在本次文件拆分中实现。

[物品查阅清单](<../../14运输分类统计/README.md>) · [数据契约](<../../14运输分类统计/06_数据契约与迁移.md>) · [货柜目录](<../03_货柜/README.md>)
