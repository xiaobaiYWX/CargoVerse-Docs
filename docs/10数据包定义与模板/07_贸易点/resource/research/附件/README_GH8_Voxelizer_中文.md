# Rhino 8 / Grasshopper 体素化电池

适用目标：Rhino 8 SR32（8.32.26160.13001）与内置 Grasshopper 1.0。

这是一个无需安装 `.gha` 的 C# Script 电池。它把输入几何体采样为边长一致的小方块，并通过 `Resolution` 调整精度。

## 安装与接线

1. 打开 Rhino 8，执行 `Grasshopper`。
2. 放置 `Maths > Script > C# Script` 电池。
3. 双击电池进入编辑器，将自动生成的 `RunScript` 方法以及下方辅助代码替换为 `GH8_Voxelizer_CSharp_Script.cs` 的全部代码。
4. 在电池上建立以下输入；名称和类型需一致：

| 输入 | Grasshopper 类型 | Access | 建议默认值 | 说明 |
|---|---|---|---:|---|
| `G` | Geometry | Item | — | 待体素化模型 |
| `Resolution` | Integer | Item | 20 | 模型包围盒最长边划分数；越大越精细 |
| `Solid` | Boolean | Item | True | 闭合模型填满内部；False 仅生成表面壳体 |
| `MaxVoxels` | Integer | Item | 250000 | 候选体素安全上限，防止 Grasshopper 卡死 |

5. 建立以下输出：

| 输出 | 内容 |
|---|---|
| `Voxels` | Box 列表，可直接预览或接 `Brep` / `Mesh` 等后续电池 |
| `Centers` | 每个保留体素的中心点 |
| `Info` | 数量、实际方块边长、网格尺寸和当前模式 |

## 使用建议

- 闭合 Brep、闭合 Mesh、闭合 Extrusion：`Solid=True`，生成实体填充体素。
- 开放 Brep、开放 Mesh、Surface、Curve：自动按一层体素厚度生成表面壳体。
- `Resolution=20` 适合预览；确认效果后逐渐提高到 40、60 或 80。
- 计算量近似随精度的三次方增长。精度从 20 提高到 40，候选体素最多约增至 8 倍。
- 若出现超过 `MaxVoxels` 的红色报错，降低 `Resolution`，或在明确机器承受能力后提高上限。

## 算法边界

- 实体模式使用“体素中心点是否位于闭合体内部”的判定。因此极薄、尖锐或小于一个体素的局部特征可能消失，这是常见的中心采样体素化行为。
- 表面模式使用中心点到几何体的最近距离，厚度约为一个体素。
- 输出为 Grasshopper `Box`，没有自动烘焙进 Rhino 文档；需要实体对象时可右键输出端或后续参数执行 Bake。

## 快速测试

在 Grasshopper 中放置一个 `Sphere`，连接到 `G`，设置：

- `Resolution = 24`
- `Solid = True`
- `MaxVoxels = 250000`

应得到由小方块填充的球形近似，并在 `Info` 中看到生成数量与体素边长。
