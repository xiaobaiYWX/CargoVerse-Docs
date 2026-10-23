# HEC CryoVault 冷冻保存柜 S 型

> **【未实现／未开放制造】仅维护定义与设计目标；不提供该专项的完整运输、制造或交易能力。**

[赫利俄斯能源集团](<../README.md>) → [CryoVault 冷冻保存柜](<README.md>) → S 型

## 职责与使用边界

独立冷冻保存线，覆盖 S/M/L；不能与防冻结共用一个模糊温控能力。

- 目标形态：独立固体 solid。
- 当前 JSON 承载：独立固体 solid。
- 当前生效保护：防潮 D。
- 完整目标保护：防潮、遮光、冷冻（目标）。
- 使用边界：不兼任防冻结温热柜；水等明确禁冻内容须提示冲突。
- 典型内容：冰块、需冻结保存且耐受冻结的封装内容；普通耐冷固体也可用。仅为例子，同形态同条件的物品不因行业或制造商被排除。
- 当前阶段：后续专项，未制造。

保护外观不等于程序效果。遮光、温控、生态维持和放射性屏蔽等未列入“当前生效保护”的部分只能作为后续结构预留，不能标成已经实装。

## 定义

| 项目 | 内容 |
| --- | --- |
| 资源 ID | `cargoverse:hec/cryovault_sd_s` |
| 定义文件 | [cryovault_sd_s.json](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_s.json>) |
| 制造商 | 赫利俄斯能源集团（`cargoverse:hec`） |
| 系列 | CryoVault 冷冻保存柜 |
| 尺寸等级 | S |
| 普通调度点 | 1 |
| 结算单位 | `cargoverse:void_byte` |
| 标签 | `series.hec.cryovault`、`not_manufacturable` |

## 数值

| 指标 | 当前定义值 |
| --- | --- |
| 容量 | 35 个实际物品（未开放制造） |
| 空柜目标质量 | 34 Kpg |
| 分类容量修正 | 无，使用定义容量 |

空重为配置目标，实际基础质量取模板结构质量与配置空重的较大值；载货质量另算。型号 ID 的后缀不替代实际尺寸或接口。

## CargoClass 兼容与保护

允许：独立固体（solid）。

当前生效保护：`cargoverse:moisture_proof`。

设计缺陷：无。未实现的目标保护不产生程序效果；准入与完整组件校验仍独立执行。

## 结构模板

| 项目 | 当前事实／制作目标 |
| --- | --- |
| 定义 | [cargoverse:hec/cryovault_sd_s](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hec/cryovault_sd_s.json>) |
| 当前实际引用 | `cargoverse:cargo/aui/atlas/aui_atlas_sd_s` |
| 当前 NBT | [Atlas S 占位结构](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/aui/atlas/aui_atlas_sd_s.nbt>)；包络 7×3×5，体积 105；标准对接接口×2 |
| 专用路径建议 | `cargoverse:cargo/hec/cryovault/hec_cryovault_sd_s`；这是原候选／设计目标，不是已批准的分配结果 |
| 制作优先级 | 后续专项：先预留职责，不为未实现机制赶工 |
| 最终采用 | 待你分配；未切换运行引用 |

**原自用模板候选：** `cargoverse:cargo/hec/cryovault/hec_cryovault_sd_s` · [原 NBT 文件](<../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hec/cryovault/hec_cryovault_sd_s.nbt>)。

只读结构检查：包络 4×9×4；标准对接接口×4；质量占位 4 个；分类占位 4 个；警示占位 20 个（槽号 0／1／2／3／4）；实体 0 个。这不是碰撞、实际质量、密封性或 Sable 连接验收。

## 制造与投放

当前无制造配方，不能把占位结构当作已开放产品。材料、费用、许可证和投放需在专项设计完成后明确，不从旧版成本或规格自动推导。

[统一制造与投放索引](<../../../08_货柜制造台/制造配方与投放总表.md>)。

## 当前 JSON

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/aui/atlas/aui_atlas_sd_s",
  "manufacturer": "cargoverse:hec",
  "display_name": "HEC CryoVault 冷冻保存柜 S 型",
  "description": "临时使用对应规格 AUI 标准干柜结构；实际承载与保护以本定义为准。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 1,
  "capacity": 35,
  "empty_mass": 34,
  "allowed_cargo_classes": [
    "solid"
  ],
  "special_designs": [
    "cargoverse:moisture_proof"
  ],
  "design_defects": [],
  "tags": [
    "series.hec.cryovault",
    "not_manufacturable"
  ],
  "cargo_class_capacity_modifiers": {}
}
```

## 验证边界

占位结构可加载不表示目标能力可用；专用模板、容量、保护、装卸和实机验证必须分别完成。已有物理货柜不因文档调整或重载自动换壳。

[返回系列](<README.md>) · [返回制造商](<../README.md>)
