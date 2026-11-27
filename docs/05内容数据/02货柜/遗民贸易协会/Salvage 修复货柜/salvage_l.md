# REX Salvage 修复货柜 L 型

## 货柜介绍

Salvage经过REX工坊的防雨与缓冲整修，旧壳体上的痕迹却常被留下。有些货柜已换过几位主人，协会的回收单可能认识他们每一个。用于集中移交回收成果。卸货单里偶尔会留下一整栏，等待有人认出其中的物件。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Salvage 修复货柜 |
| 文档型号代号 | `rex/salvage_l` |
| 规格 | L |
| 运输介质 | solid |
| 容量 | 16384 件 |
| 定义空重 | 145 Kpg |
| 调度点 | 4 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按单件计数，组只决定装卸步长。最大堆叠64时满载为256组；每件0.1 Kpg的货物装满后货重1638.4 Kpg，不含柜体。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 缓冲衬垫 | `cargoverse:cushioning` | `{"level":1,"velocity_change_bonus":2}` |
| 防水柜体 | `cargoverse:waterproof_body` | `{}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/rex/salvage_g2/rex_salvage_g2_l` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/rex/salvage/salvage_l.nbt` |
| 尺寸 X×Y×Z | 12×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/rex/salvage_g2/rex_salvage_g2_l.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

测试贸易点 A、测试贸易点 B；遗民遗产贸易港

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | L |
| 制造商声望 | cargoverse:rex／2级 |
| 蓝图打印费 | 320 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 128 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 32 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 16 |
| 特殊材料 | 缓冲组件（`cargoverse:cushioning_module`） | 4 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:rex/salvage_lm_l` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/rex/salvage_lm_l.json) |
| 制造配方 ID | `cargoverse:rex/salvage_lm_l` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/rex/salvage_lm_l.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "template": "cargoverse:cargo/rex/salvage_g2/rex_salvage_g2_l",
  "manufacturer": "cargoverse:rex",
  "display_name": "REX Salvage 修复货柜 L 型",
  "description": "Salvage经过REX工坊的防雨与缓冲整修，旧壳体上的痕迹却常被留下。有些货柜已换过几位主人，协会的回收单可能认识他们每一个。用于集中移交回收成果。卸货单里偶尔会留下一整栏，等待有人认出其中的物件。",
  "size_class": "L",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 4,
  "capacity": 16384,
  "empty_mass": 145,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.rex.salvage"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {
    "cargoverse:cushioning": {
      "level": 1,
      "velocity_change_bonus": 2
    },
    "cargoverse:waterproof_body": {}
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
