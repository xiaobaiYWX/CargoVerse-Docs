# HEC Reactor 屏蔽封装柜 M 型

> **【未实现／未开放制造】仅维护定义与设计目标；不提供该专项的完整运输、制造或交易能力。**

[赫利俄斯能源集团](<../README.md>) → [Reactor 屏蔽封装柜](<README.md>) → M 型

## 职责与使用边界

为明确存在的放射性封装固体提供屏蔽；没有有效需求时不优先投放。保留 M/L/X，不增 S。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防潮 D、定向固定 O。
- 完整目标保护：放射性屏蔽、防潮、定向固定。
- 使用边界：不提供液体罐、气密、耐压或通用防腐；不增 S。
- 典型内容：明确有放射性要求的封装固体，也可承接普通同形态物品。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：需求确认后推进，未制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:hec/reactor_hd_m` |
| 定义文件 | [reactor_hd_m.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_m.json>) |
| 制造商 | 赫利俄斯能源集团（`cargoverse:hec`） |
| 系列 | Reactor 屏蔽封装柜 |
| 尺寸等级 | M |
| 普通调度点 | 2 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.reactor`、`not_manufacturable` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 65 个实际物品（未开放制造） |
| 空柜目标质量 | 90 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:moisture_proof`、`cargoverse:keep_upright`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:hec/reactor_hd_m](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/reactor_hd_m.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_m` |
| 当前 NBT | [Atlas M 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_m.nbt>)；包络 9×4×6，体积 216；标准对接接口×4 |
| 专用路径建议 | `cargoverse:cargo/hec/reactor/hec_reactor_hd_m`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**原自用模板候选：** `cargoverse:cargo/hec/reactor/hec_reactor_hd_m` · [原 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/reactor/hec_reactor_hd_m.nbt>)。

只读结构检查：包络 10×6×5；重型连接点×4；质量占位 2 个；分类占位 0 个；警示占位 10 个（槽号 0／1／2／3／4）；实体 0 个。这不是碰撞、实际质量、密封性或 Sable 连接验收。

## 制造与投放

当前无制造配方，不能把占位结构当作已开放产品。材料、费用、许可证和投放需在专项设计完成后明确，不从旧版成本或规格自动推导。

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_m",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC Reactor 屏蔽封装柜 M 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "M",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 2,
  "capacity": 65,
  "empty_mass": 90,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:moisture_proof",
    "cargoverse:keep_upright"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.reactor",
    "not_manufacturable"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

占位结构可加载不表示目标能力可用；专用模板、容量、保护、装卸和实机验证必须分别完成。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
