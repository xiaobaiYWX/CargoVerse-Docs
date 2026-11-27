# REX Reliquary 遗物保藏柜 S 型

## 货柜介绍

Reliquary用缓冲、隔热和遮光照看打捞发现。某些交接单采用研究院常用的记录格式，收货单位却被省略；REX只提醒船员别把附件弄丢。用于少量珍贵回收物。随柜记录有时只写着发现地点，以及一句“请保留原有排列”。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Reliquary 遗物保藏柜 |
| 文档型号代号 | `rex/reliquary_s` |
| 规格 | S |
| 运输介质 | solid |
| 容量 | 2048 件 |
| 定义空重 | 36 Kpg |
| 调度点 | 1 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按单件计数，组只决定装卸步长。最大堆叠64时满载为32组；每件0.1 Kpg的货物装满后货重204.8 Kpg，不含柜体。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 缓冲衬垫 | `cargoverse:cushioning` | `{"level":3,"velocity_change_bonus":8}` |
| 真空隔层 | `cargoverse:vacuum_insulation` | `{"level":1}` |
| 遮光结构 | `cargoverse:light_blocking` | `{"level":1,"reduction":15}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/rex/reliquary_g2/rex_reliquary_g2_s` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/rex/reliquary/reliquary_s.nbt` |
| 尺寸 X×Y×Z | 4×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/reliquary_g2/rex_reliquary_g2_s.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | S |
| 制造商声望 | cargoverse:rex／0级 |
| 蓝图打印费 | 100 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 32 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 8 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 4 |
| 特殊材料 | 缓冲组件（`cargoverse:cushioning_module`） | 4 |
| 特殊材料 | 高纯陶瓷粉（`cargoverse:high_purity_ceramic_powder`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:rex/reliquary_lm_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/reliquary_lm_s.json) |
| 制造配方 ID | `cargoverse:rex/reliquary_lm_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/rex/reliquary_lm_s.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:rex",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/rex/reliquary_g2/rex_reliquary_g2_s",
  "display_name": "REX Reliquary 遗物保藏柜 S 型",
  "description": "Reliquary用缓冲、隔热和遮光照看打捞发现。某些交接单采用研究院常用的记录格式，收货单位却被省略；REX只提醒船员别把附件弄丢。用于少量珍贵回收物。随柜记录有时只写着发现地点，以及一句“请保留原有排列”。",
  "size_class": "S",
  "dispatch_points": 1,
  "empty_mass": 36,
  "allowed_cargo_classes": [
    "solid"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.rex.reliquary"
  ],
  "capacity": 2048,
  "abilities": {
    "cargoverse:cushioning": {
      "level": 3,
      "velocity_change_bonus": 8
    },
    "cargoverse:vacuum_insulation": {
      "level": 1
    },
    "cargoverse:light_blocking": {
      "level": 1,
      "reduction": 15
    }
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
