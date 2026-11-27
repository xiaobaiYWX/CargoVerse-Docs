# VBS Seedbox 田园货柜 S型

## 货柜介绍

Seedbox没有调温或照明设备，先供新人运输普通物资。隔壁培养站的产量可能足以填满许多这样的柜子，却不会因此缩短装卸教学。饲养员批注：不用数外面有几只羊，先数你带了几个空柜。

## 型号与承载

| 项目 | 现行值 |
| --- | --- |
| 系列 | Seedbox 田园货柜 |
| 文档型号代号 | `vbs/seedbox_s` |
| 规格 | S |
| 运输介质 | solid |
| 容量 | 2048 件 |
| 定义空重 | 12 Kpg |
| 调度点 | 0 |
| 接口 | 统一标准接口；型号代号不再包含接口缩写 |

容量按单件计数，组只决定装卸步长。最大堆叠64时满载为32组；每件0.1 Kpg的货物装满后货重204.8 Kpg，不含柜体。

实际空重取定义空重与结构质量的较大值。表中数值不是结构实测质量，起吊与满载运输仍需实机验收。

## 保护能力

无能力，`abilities: {}`。封闭外观和展示贴花不会提供隐含保护。

容量修正：`{}`。运输条件与能力的对应规则见[能力规范](../../../../04数据规范/货柜/能力/README.md)。

## 模板与制作状态

| 项目 | 现行值 |
| --- | --- |
| 模板状态 | 已接入；发布文件存在，无缺失模板 |
| 模板资源 ID | `cargoverse:start_cargo/vbs/seedbox_s` |
| 导出相对路径 | `generated/cargoverse/structures/start_cargo/vbs/seedbox_s.nbt` |
| 尺寸 X×Y×Z | 4×5×5 格 |
| 发布结构文件 | [NBT](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/structure/start_cargo/vbs/seedbox_s.nbt) |

使用本系列独立初始模板。尺寸沿现有模板记录；对接、结构质量和满载表现仍按[实运验收](../../制作与实运验收.md)检查。

## 蓝图获取与制造

注册本制造商许可证时赠送一张已打印蓝图；所有打印目录排除本型号。注销保留已制造货柜，重新注册再次赠图，但八品牌共用每名玩家一个初始柜的名额（含施工占用）。

| 项目 | 当前要求 |
| --- | --- |
| 许可证 | S |
| 制造商声望 | cargoverse:vbs／0级 |
| 蓝图打印费 | 0 VB |
| 施工时间 | 400 tick（20 TPS时20秒） |

材料按实体物品件数消耗，打印阶段不扣材料。初始型号的0费用不表示能在打印机中领取。

| 层次 | 材料 | 件数 |
| --- | --- | ---: |
| 主材料 | 铁锭（`minecraft:iron_ingot`） | 16 |
| 辅材料 | 标准紧固件箱（`cargoverse:standard_fasteners`） | 4 |
| 辅材料 | 工业构件箱（`cargoverse:industrial_components`） | 2 |

[产业物资获取与生产](../../../01运输物品/04_产业物资.md) · [共用制造规则](../../../03贸易点/蓝图投放/制造配方与投放总表.md)

## 运行资源对应

文档型号代号用于统一查阅和制作命名，**不是已注册的新资源ID**。本轮未迁移运行资源；指令、配方和数据包引用仍使用下列实际ID。旧名称不表示第二个产品系列或不同接口。

| 资源 | 当前 ID／来源 |
| --- | --- |
| 实际货柜定义 ID | `cargoverse:vbs/seedbox_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_containers/vbs/seedbox_s.json) |
| 制造配方 ID | `cargoverse:vbs/seedbox_s` · [JSON](../../../../../../CargoVerse-NeoForge-1.21.1/src/main/resources/data/cargoverse/cargo_manufacturing_recipes/vbs/seedbox_s.json) |

<details>
<summary>完整现行货柜定义</summary>

```json
{
  "schema_version": 1,
  "template": "cargoverse:start_cargo/vbs/seedbox_s",
  "manufacturer": "cargoverse:vbs",
  "display_name": "VBS Seedbox 田园货柜 S型",
  "description": "Seedbox没有调温或照明设备，先供新人运输普通物资。隔壁培养站的产量可能足以填满许多这样的柜子，却不会因此缩短装卸教学。饲养员批注：不用数外面有几只羊，先数你带了几个空柜。",
  "size_class": "S",
  "trade_currency": "cargoverse:void_byte",
  "dispatch_points": 0,
  "capacity": 2048,
  "empty_mass": 12,
  "allowed_cargo_classes": [
    "solid"
  ],
  "tags": [
    "series.vbs.seedbox",
    "starter"
  ],
  "cargo_class_capacity_modifiers": {},
  "abilities": {}
}
```

</details>

[本系列](README.md) · [制造商目录](../README.md)
