# SPL Cistern 常规液罐 X 型

## 货柜介绍

Cistern把液体运输纳入云港物流的日常班表。密封罐体服务于常规补给，采购单上没有复杂的环境调节要求，只有收货地址和下一次补货日期。适合区域集中供应。它到港时，往往有几家收货单位同时来确认卸货次序。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Cistern 常规液罐 |
| 文档型号代号 | `spl/cistern_x` |
| 规格 | X |
| 运输介质 | liquid |
| 容量 | 512 桶 |
| 定义空重 | 260 Kpg |
| 调度点 | 6 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

1桶为1000 mB，原生载荷按mB保存；满载为512000 mB。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

| 能力 | 配置 ID | 完整参数 |
| --- | --- | --- |
| 密封结构 | `cargoverse:sealing` | `{"level":1}` |

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:cargo/spl/cistern_g2/spl_cistern_g2_x` |
| 导出相对路径 | `generated/cargoverse/structures/cargo/g2/spl/cistern/cistern_x.nbt` |
| 尺寸 X×Y×Z | 12×9×10 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/cargo/spl/cistern_g2/spl_cistern_g2_x.nbt) |

G2模板按本系列命名，不使用其他系列作占位。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

测试贸易点 A、测试贸易点 B

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | X |
| 制造商声望 | cargoverse:spl／3级 |
| 蓝图打印费 | 720 VB |
| 施工时间 | 800 tick（20 TPS时40秒） |

材料按实体物品件数消耗，打印阶段不扣材料。蓝图获取仍需满足所列许可证及声望要求。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铜锭（`minecraft:copper_ingot`） | 256 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 64 |
| 辅材料 | 密封接头组（`cargoverse:sealing_joints`） | 32 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:spl/cistern_sd_x` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/spl/cistern_sd_x.json) |
| 制造配方 ID | `cargoverse:spl/cistern_sd_x` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/spl/cistern_sd_x.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "manufacturer": "cargoverse:spl",
  "trade_currency": "cargoverse:void_byte",
  "template": "cargoverse:cargo/spl/cistern_g2/spl_cistern_g2_x",
  "display_name": "SPL Cistern 常规液罐 X 型",
  "description": "Cistern把液体运输纳入云港物流的日常班表。密封罐体服务于常规补给，采购单上没有复杂的环境调节要求，只有收货地址和下一次补货日期。适合区域集中供应。它到港时，往往有几家收货单位同时来确认卸货次序。",
  "size_class": "X",
  "dispatch_points": 6,
  "empty_mass": 260,
  "allowed_cargo_classes": [
    "liquid"
  ],
  "cargo_class_capacity_modifiers": {},
  "tags": [
    "series.spl.cistern"
  ],
  "capacity": 512,
  "abilities": {
    "cargoverse:sealing": {
      "level": 1
    }
  }
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
