# 实际物品基础属性与运输条件

更新：2026-10-28。每个物品一份基础属性，新增 schema 3 的 `transport_conditions` 选择源码注册类型并直接填写参数。货柜能力先改变五组实际状态，再由条件决定货损，围护与封存仍直接比较。不建立共享条件文件、成员标签或按 ID 独立扣量的 Handler。完整目标见[未完成规格与参数](../../设计草案/待完成事项清单.md#运输条件与能力专项)，运行接入范围见[正式运行文档](../../01货柜系统/01核心系统/14_运输数值运行时.md#源码注册类型已接入的配置架构)。

## 目录与身份

路径：`data/<物品命名空间>/cargoverse_item_properties/<形态>/<物品路径>.json`。

- `data/minecraft/cargoverse_item_properties/solid/cake.json` 对应 `minecraft:cake`。
- `data/create/cargoverse_item_properties/solid/shaft.json` 对应 `create:shaft`。

文件内 `form` 必须与目录一致；物品 ID 由命名空间和路径推导。同一路径按数据包优先级覆盖，不同目录重复声明同一物品则整代拒绝。未知物品、空气、错误参数及无效静态贴花引用不能静默降级为默认。

三种形态为 solid／liquid／living；当前实际物品均为 solid，包括细粉和瓶装药水。直接泵入的液体使用独立流体属性与载荷；气态 Fluid 统一使用 liquid 属性、载荷与仓储，活体尚未开放。

## schema 3：注册类型与直接参数

新增或改写属性使用 schema 3。例如围护需求的局部内容：

```json
{
  "schema_version": 3,
  "form": "solid",
  "unit_mass": 0.1,
  "decal": "cargoverse:decal_none",
  "admission_policy": "standard",
  "transport_conditions": {
    "cargoverse:powder": {
      "loss": {"grace_ticks": 0, "interval_ticks": 1200, "amount": 1}
    }
  }
}
```

schema 3 不能同时写旧 `transport` 或 `transport_requirements`。未知 ID、参数、重复键与同一边界重复声明报错。已注册的 13 类条件均可执行，包括速度窗口易碎、正放、干燥、光照下限与推荐目标；候选参数运行不等于正式内容平衡已验收。

## schema 3 示例：当前内置玻璃

以下与当前候选资源一致，不代表最终平衡：

```json
{
  "schema_version": 3,
  "form": "solid",
  "unit_mass": 0.1,
  "decal": "cargoverse:decal_construction_material",
  "admission_policy": "standard",
  "transport_conditions": {
    "cargoverse:fragile": {"max_velocity_change": 10, "damage_amount": 1}
  }
}
```

玻璃具有易碎条件。货柜缓冲直接增加速度变化耐受，相隔 10 tick（0.5 秒）的相邻两次参考点速度向量差严格超过最终耐受才按独立事件扣 1pcs。例如缓冲加 8 后耐受为 18；不是缓冲柜删除该条件或免疫所有冲击，不采用 J 或加速度单位。

| 字段 | 职责 |
| --- | --- |
| `schema_version` | 新注册格式使用 3；现有资源暂用的内联格式为 2，旧资料为 1；各版本输入不得叠加 |
| `form` | 基本装载形态，必须与目录一致 |
| `unit_mass` | 每组质量 Kpg（组大小取精确物品的最大堆叠量），内置用 0～1 的整数或一位小数；零质量仍占容量 |
| `decal` | 显式静态贴花 ID，不从形态或条件推导 |
| `admission_policy` | standard／empty_storage／blocked，独立验证组件与安全准入 |
| `transport_conditions` | schema 3 的源码注册 ID → 参数对象；不由数据包新增行为或图标 |
| `transport` | schema 2 的过渡内联格式；impact 使用 max_velocity_change／damage_amount；旧 tolerance 字段拒绝，不能重解释旧 J |

细粉填写围护需求 2，易碎品填写冲击耐受，易腐坏食品填写保存预算和温区老化曲线；不填写柜型白名单、货柜能力名称或保鲜免疫开关。可组合多个条件；具体字段和 JSON 示例见[类型与参数](../../01货柜系统/01核心系统/15_运输类型与参数.md)。价格、经验、完整度和容量权重不在此处维护。`unit_mass` 保留字段名和当前数值，现行含义统一为每组质量；不是沿用每个物品计重。原生货损 `amount`／`damage_amount` 仍按 pcs，不放大为整组。

schema 3 无额外条件时省略 `transport_conditions` 或写空对象；每个已声明类型的必要参数必须齐全。围护／密封需求 0 不生效。亮度上限 0、温度边界 0、压力上限 0 是有效物理值；不得据此关闭条件。损耗数量必须为正整数。旧 schema 2 的整组数值 0 简写只保留在过渡输入中，不套用于注册参数对象。

## 缺失数据与安全边界

缺少文件时使用源码默认：solid、每组 0.1 Kpg、standard、无额外条件、`cargoverse:decal_none`。不提供默认 JSON，不按名称、配方或行业猜测运输条件。错误文件拒绝发布整代，不当作缺失文件回退。

`empty_storage` 只调用已审阅的真实验空适配；`data/cargoverse/item_storage_adapters.json` 维护适配 ID，不保存物性，也不能由一份属性文件授权未知容器。非空嵌套容器和生物桶等继续独立检查。

## 冻结、显示与维护

- 一柜一种实际物品及完整组件状态，1 组物品占 1 容量，组大小从精确 ItemStack 的最大堆叠量读取并冻结。保护不足通常只提示风险，不恢复用途／粉末白名单。
- 首次成功装载冻结物品属性及当时货柜能力、调温约束、换算表；途中重载不改写既有会话。追加必须兼容且不刷新年龄，卸空清会话。
- 贴花使用声明值。数值警示图标解释物品条件；护目镜、装载终端、制造台和航运档案不以旧正负词条 ID 判断效果。
- 佩戴护目镜时仅显示必要准入提示及有效运输条件名称；普通无需求物品不增加提示，不显示形态或默认来源。
- 客户端使用已有分包目录与数值特性位集；碎料／粉料／易挥发分别投影，不发送高频逐物品属性请求。运行状态见[运输数值运行时](../../01货柜系统/01核心系统/14_运输数值运行时.md)，版本统一见[当前数据契约](../../01货柜系统/01核心系统/07_运行时与存档.md#当前数据契约)。

2315 份文件是唯一维护源。当前玻璃与 10 个新警示贴花物品采用 schema 3，其他物品仍为 schema 1；大部分内置文件仍待数值赋值。schema 1 的旧需求仅作待清理输入资料，不执行旧损耗或生成有效标签，不能直接把其中字母复制为新能力。

修改参数先改相应 JSON，再同步文档。按变更范围运行解析、准入、保存、求值和必要的注册测试；未支持的旧资料检查脚本不作为新物性通过的证明。最终内容平衡、客户端布局和真实运输路线仍需验收。

[物品查阅清单](../../14运输分类统计/README.md) · [数据与冻结契约](../../14运输分类统计/06_数据契约与迁移.md) · [货柜目录](../03_货柜/README.md)
