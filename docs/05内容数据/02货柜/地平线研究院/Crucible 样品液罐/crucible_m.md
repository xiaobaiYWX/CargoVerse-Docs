# HRI Crucible 样品液罐 M 型

## 货柜介绍

Crucible把液体样品的密封、温压调节与遮光安排在同一罐体内。地平线研究院习惯随货附上观察记录，未确认的性质会留下空白，而不会写成“安全”。用于少量样液的复核运输。研究员宁愿多等一班船，也不愿让不同批次的记录混在一起。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Crucible 样品液罐 |
| 文档型号代号 | `hri/crucible_m` |
| 规格 | M |
| 运输介质 | liquid |
| 容量 | 64 桶 |
| 定义空重 | 80 Kpg |
| 调度点 | 2 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

1桶为1000 mB，原生载荷按mB保存；满载为64000 mB。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 密封结构 | `cargoverse:sealing` | `{"level":1}` |
| 主动调温 | `cargoverse:thermal_control` | `{"level":1}` |
| 气压调节 | `cargoverse:pressure_control` | `{"level":1}` |
| 遮光结构 | `cargoverse:light_blocking` | `{"level":1,"reduction":15}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/hri/crucible_g2/hri_crucible_g2_m` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/gri/crucible/crucible_m.nbt` |
| 尺寸 X×Y×Z | 8×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/hri/crucible_g2/hri_crucible_g2_m.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

地平线科研贸易港；测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | M |
| 制造商声望 | cargoverse:hri／1级 |
| 蓝图打印费 | 220 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铜锭（`minecraft:copper_ingot`） | 64 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 16 |
| 辅材料 | 密封接头组（`cargoverse:sealing_joints`） | 8 |
| 特殊材料 | 调温机组（`cargoverse:thermal_control_unit`） | 2 |
| 特殊材料 | 稳压组件（`cargoverse:pressure_regulator`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:hri/crucible_si_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/hri/crucible_si_m.json) |
| 制造配方 ID | `cargoverse:hri/crucible_si_m` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/hri/crucible_si_m.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:hri",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/hri/crucible_g2/hri_crucible_g2_m",
  "display_name": "HRI Crucible 样品液罐 M 型",
  "description": "Crucible把液体样品的密封、温压调节与遮光安排在同一罐体内。地平线研究院习惯随货附上观察记录，未确认的性质会留下空白，而不会写成“安全”。用于少量样液的复核运输。研究员宁愿多等一班船，也不愿让不同批次的记录混在一起。",
  "size_class": "M",
  "dispatch_points": 2,
  "empty_mass": 80,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.hri.crucible"
  ],
  "capacity": 64,
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    },
    "cargoverse:thermal_control": {
      "level": 1
    },
    "cargoverse:pressure_control": {
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
