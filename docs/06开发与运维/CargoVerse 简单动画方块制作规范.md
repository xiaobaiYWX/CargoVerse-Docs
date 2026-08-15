## 1. 当前动画系统的定位

当前框架适合机械方块的简单部件动画，包括：

|动画|当前支持|示例|
|---|---|---|
|平移|支持 X/Y/Z|活塞升降、舱门滑动|
|旋转|支持 X/Y/Z|转子、把手、舱盖|
|缩放|支持 X/Y/Z|能量核心呼吸、管道膨胀|
|状态切换平滑过渡|支持|关闭 → 开启|
|持续匀速旋转|支持|风扇、转盘|
|持续往复移动|支持|上下浮动、机械振动|
|持续呼吸缩放|支持|发光核心、压力管|
|多个活动部件|支持|双舱门、多根活塞|
|动画叠加|代码侧支持|展开后继续旋转|
|状态切换粒子|支持|启动火花、停机烟雾|

暂不支持：

- Blockbench 时间轴动画直接导入
- 骨骼和蒙皮  
    -复杂关键帧序列
- 贝塞尔动画曲线编辑
- 一个模型元素的形状变形
- GeckoLib 动画格式
- 粒子可视化编辑器

因此，美术组不需要在 Blockbench 中制作关键帧动画。美术交付的核心是：

1. 静态主体模型；
2. 每个可动部件的独立模型；
3. 每个部件的旋转或缩放轴心；
4. 动画前后的目标位置和角度；
5. 粒子纹理。

---

# 2. 动画方块的资源组成

一个动画方块一般应拆成：

```
animated_machine/
├─ block.json             # 静态主体
├─ item.json              # 物品展示模型
├─ rotor.json             # 活动部件：转子
├─ hatch.json             # 活动部件：舱盖
└─ piston.json            # 活动部件：活塞
```

游戏内结构：

```
静态主体
└─ 由普通方块模型渲染

活动部件
├─ rotor.json
├─ hatch.json
└─ piston.json
```

程序会分别加载活动部件，并在运行时对它们平移、旋转或缩放。

## 最重要的拆分原则

任何需要移动的元素都必须从静态主体中删除。

错误示例：

```
block.json
├─ 外壳
└─ 舱门       ← 舱门仍在主体中

hatch.json
└─ 舱门       ← 运行时又渲染一次
```

这会出现两个舱门重叠。

正确示例：

```
block.json
└─ 外壳

hatch.json
└─ 舱门
```

---

# 3. Blockbench 项目设置

建议创建：

```
格式：Java Block/Item
模型尺寸：16 × 16 × 16
纹理尺寸：16、32、64 等 2 的幂
坐标范围：原则上以 0～16 为一个方块
```

推荐让静态主体和所有活动部件都使用相同的 Blockbench 坐标空间。

例如：

```
方块中心：
Blockbench 坐标 = (8, 8, 8)
游戏模型坐标   = (0.5, 0.5, 0.5)
```

换算规则：

```
游戏坐标 = Blockbench 坐标 ÷ 16
```

例如舱门轴心：

```
Blockbench Origin: (8, 4, 2)
游戏 Pivot:        (0.5, 0.25, 0.125)
```

## 不要分别把活动部件移动回原点

假设转子原本位于方块中心：

```
转子中心 = (8, 8, 8)
```

导出 `rotor.json` 时，应继续保留这个位置。不要为了“单独导出”将其移动到 `(0, 0, 0)`。

程序会在原方块坐标空间内渲染它。

---

# 4. 推荐的 Blockbench 分组方式

建议按最终导出的模型建立顶层组：

```
animated_machine
├─ static
│  ├─ casing
│  ├─ base
│  └─ frame
│
├─ animated_rotor
│  ├─ rotor_core
│  └─ rotor_blades
│
├─ animated_hatch
│  ├─ hatch_panel
│  └─ hatch_handle
│
└─ animated_piston
   ├─ piston_head
   └─ piston_rod
```

导出时：

|Blockbench 组|输出文件|
|---|---|
|`static`|`block.json`|
|`animated_rotor`|`rotor.json`|
|`animated_hatch`|`hatch.json`|
|`animated_piston`|`piston.json`|

Blockbench 中的组名只是制作约定，游戏不会自动把组识别为动画骨骼。

---

# 5. 轴心制作规范

旋转和缩放都必须提供轴心。

## 旋转轴心

例如舱盖绕底边打开：

```
舱盖几何中心：(8, 10, 3)
实际旋转轴心：(8, 4, 2)
旋转轴：X
角度范围：0° → -75°
```

这里不能把轴心填成舱盖几何中心，否则舱盖会围绕中央旋转。

常见轴心：

|部件|推荐轴心|
|---|---|
|风扇、转子|几何中心|
|舱门|铰链中心|
|指针|指针底端|
|操作杆|杆的安装点|
|活塞|通常不旋转，仅平移|
|呼吸核心|几何中心|
|伸缩机械臂|对应关节中心|

## 缩放轴心

缩放同样围绕指定轴心发生。

例如能量核心从中心呼吸：

```
Pivot = 核心几何中心
Scale = 1.0 → 1.08
```

如果轴心放在模型底部，缩放效果会表现为向上生长。

## 轴心交付格式

建议美术在交付说明中同时提供 Blockbench 和游戏坐标：

```
部件：hatch
轴心 BB：(8, 4, 2)
轴心 MC：(0.5, 0.25, 0.125)
旋转轴：X
关闭角度：0°
开启角度：-75°
```

---

# 6. 当前支持的状态切换动画

状态切换动画表示方块从一种状态平滑变成另一种状态。

例如：

```
关闭状态
├─ 舱盖角度：0°
├─ 活塞高度：0
└─ 核心缩放：0.8

开启状态
├─ 舱盖角度：-75°
├─ 活塞高度：0.25 格
└─ 核心缩放：1.0
```

当前支持两种平滑方式。

## LINEAR

以近似固定速度追踪目标值：

```
0.0 → 0.1 → 0.2 → 0.3 → ... → 1.0
```

适合：

- 舱门开合
- 活塞升降
- 机械部件滑动
- 固定速度旋转到目标位置

特点是机械感较强，完成时间相对明确。

## EXPONENTIAL

开始变化较快，接近目标时逐渐减速：

```
0.0 → 0.5 → 0.75 → 0.875 → ... → 1.0
```

适合：

- 操作杆
- 仪表指针
- 发光强度
- 热量和能量表现
- 柔和缩放
- 需要自然减速的部件

## 中途反向

两种模式都允许状态在动画未结束时反转。

例如舱门只打开一半时收到关闭指令，会直接从当前位置平滑关闭，不会跳回起点。

---

# 7. 当前支持的持续动画

持续动画根据客户端渲染时间计算，不需要美术制作动画帧。

## 持续旋转

适合：

- 风扇
- 转子
- 齿轮
- 扫描器
- 能量环

美术需要提供：

```
部件：rotor
轴心：(8, 8, 8)
旋转轴：Z
旋转速度建议：4°/tick
旋转方向：顺时针
播放状态：ACTIVE
```

支持正负速度：

```
4°/tick  = 正向旋转
-4°/tick = 反向旋转
```

## 往复移动

采用正弦曲线，在两个方向之间连续移动。

适合：

- 上下浮动
- 左右扫描
- 轻微机械振动
- 悬浮核心

需要提供：

```
移动轴：Y
中心位置：原始位置
振幅：2 px
周期：40 tick
播放状态：ACTIVE
```

像素换算：

```
2 px = 2 / 16 = 0.125 格
```

## 呼吸缩放

以 `1.0` 为中心周期缩放：

```
0.95 → 1.0 → 1.05 → 1.0 → 0.95
```

适合：

- 发光核心
- 能量团
- 软质管道
- 警告灯
- 魔法或科技晶体

需要提供：

```
缩放轴：XYZ
轴心：模型中心
振幅：0.05
周期：30 tick
播放状态：ACTIVE
```

建议振幅范围：

```
机械部件：0.01～0.03
能量部件：0.03～0.08
夸张效果：不建议超过 0.15
```

## 状态切换与持续动画叠加

可以先通过状态过渡展开，再持续旋转：

```
IDLE
└─ 转子缩在机器内部，不旋转

STARTING
├─ 转子向外移动
└─ 转速逐渐增加

ACTIVE
├─ 转子保持展开
└─ 持续旋转
```

美术应分别说明“状态姿态”和“持续动作”。

---

# 8. 方块朝向注意事项

模型通常以一个标准方向制作，代码再根据方块朝向旋转整个模型。

项目需要统一约定默认正面。建议：

```
Blockbench 默认正面：北面
Minecraft Direction：NORTH
```

美术交付时必须注明默认正面。

不要为东、南、西方向分别制作四套活动模型，除非各方向外观确实不同。

活动部件的轴心和移动方向通常使用模型局部坐标。例如：

```
舱门向模型正前方移动
```

程序会先根据方块朝向旋转整体，再应用对应动画。

---

# 9. 模型边界与剔除

活动部件在动画过程中可能移出一个方块范围。

例如：

```
活塞向上移动 10 px
舱门向侧面滑动 14 px
机械臂伸出相邻方块
```

美术需要在交付说明中给出最大运动范围：

```
最小边界：(-2, 0, 0)
最大边界：(18, 26, 16)
```

单位可使用 Blockbench 像素。

程序侧需要据此扩大方块实体的渲染包围盒，否则玩家在某些视角下可能看到活动部件突然消失。

---

# 10. 纹理和 UV 规范

静态主体与活动部件可以共用一张纹理：

```
textures/block/animated_machine.png
```

也可以拆分：

```
textures/block/animated_machine/base.png
textures/block/animated_machine/rotor.png
textures/block/animated_machine/emissive.png
```

建议：

- 优先共用纹理图集，减少资源数量。
- 活动部件仍使用正常方块 UV。
- 需要染色的粒子纹理使用白色或灰度。
- 不在模型中绘制运动模糊；如有需要应由独立半透明部件实现。
- 避免完全重合的面，防止 Z-fighting。
- 活动部件闭合时与主体表面至少保留微小距离。

---

# 11. 粒子美术制作规范

当前框架提供一种可参数化的通用粒子，调用时可以设置：

- RGB 颜色
- 粒子大小
- 生命周期
- 重力
- 初速度
- 发射数量
- 发射范围
- 发射速度

因此，同一张白色粒子纹理可以通过代码生成不同颜色。

## 粒子纹理目录

```
assets/cargoverse/textures/particle/
├─ machine_spark.png
├─ energy_glow.png
└─ pressure_smoke.png
```

对应定义：

```
assets/cargoverse/particles/
└─ simple_effect.json
```

## 单帧粒子

推荐尺寸：

```
8×8
16×16
32×32
```

纹理应带透明背景。

适合：

- 火花
- 光点
- 小型烟雾
- 能量颗粒

## 多帧粒子

当前粒子支持在生命周期内按顺序播放多张 Sprite：

```
{
  "textures": [
    "cargoverse:particle/machine_spark_0",
    "cargoverse:particle/machine_spark_1",
    "cargoverse:particle/machine_spark_2",
    "cargoverse:particle/machine_spark_3"
  ]
}
```

实际纹理位置：

```
textures/particle/machine_spark_0.png
textures/particle/machine_spark_1.png
textures/particle/machine_spark_2.png
textures/particle/machine_spark_3.png
```

注意，粒子 JSON 中的路径不包含 `textures/` 和 `.png`。

## 可染色粒子

如果粒子由程序指定颜色，建议使用：

```
白色主体
灰色亮度变化
透明背景
```

不要提前绘制强烈的固定色彩，否则程序颜色会与纹理颜色相乘，导致最终颜色偏暗或失真。

---

# 12. 状态切换粒子说明

美术交付时应说明粒子的触发时机：

```
粒子名称：machine_start
触发：IDLE → ACTIVE
位置：方块中心上方 4 px
数量：12
颜色：#78E8FF
大小：0.12
寿命：16～20 tick
速度方向：向外
```

常见触发方式：

|事件|粒子示例|
|---|---|
|启动|蓝色火花、能量光点|
|停止|灰烟、余热粒子|
|锁定成功|环形闪光|
|锁定失败|红色火花|
|工作中|低频蒸汽、散热粒子|
|过载|高频火花和烟雾|
|开门|少量灰尘或气压释放|
|对接完成|接口周围环形粒子|

持续工作粒子应尽量低频，不建议每个方块每 Tick 大量生成。

---

# 13. 推荐交付表

每个动画方块建议同时提交一份 Markdown 或表格说明：

```
方块 ID：
默认正面：
Blockbench 文件：
纹理尺寸：

静态模型：
- block.json

活动部件 1：
- 名称：
- 文件：
- Pivot BB：
- Pivot MC：
- 初始位置：
- 初始旋转：
- 初始缩放：

活动部件 2：
- 名称：
- 文件：
- Pivot BB：
- Pivot MC：
- 初始位置：
- 初始旋转：
- 初始缩放：

逻辑状态：
- IDLE：
- ACTIVE：
- ERROR：

状态切换：
- IDLE → ACTIVE
- 模式：LINEAR / EXPONENTIAL
- 建议速度：
- 平移：
- 旋转：
- 缩放：

持续动画：
- 播放状态：
- 类型：旋转 / 往复 / 呼吸
- 轴：
- 速度或周期：
- 幅度：

粒子：
- 触发条件：
- 生成位置：
- 纹理：
- 颜色：
- 大小：
- 数量：
- 生命周期：
- 初速度：

最大动画边界：
```

# 14. 完整示例

以“能源反应器”为例：

```
模型：
├─ reactor/block.json
├─ reactor/core.json
└─ reactor/ring.json
```

状态：

```
IDLE
├─ core 缩放：0.8
├─ core 高度：0 px
└─ ring 角度：0°

ACTIVE
├─ core 缩放：1.0
├─ core 高度：2 px
└─ ring 持续旋转
```

制作参数：

```
core:
  Pivot BB: (8, 8, 8)
  IDLE Scale: 0.8
  ACTIVE Scale: 1.0
  ACTIVE Translation Y: 2 px
  Transition: EXPONENTIAL
  Chase Speed: 0.1

ring:
  Pivot BB: (8, 8, 8)
  Rotation Axis: Y
  Active Speed: 3°/tick
```

粒子：

```
IDLE → ACTIVE:
  颜色：#55DDFF
  数量：16
  大小：0.10
  寿命：20 tick
  位置：核心周围

ACTIVE:
  每 10 tick 生成 1～2 个光点
```

## 最关键的四条要求

给美术组可以重点强调：

1. 每个需要运动的部件必须导出为独立模型。
2. 所有模型必须保留在同一个 0～16 方块坐标空间。
3. 每个旋转或缩放部件必须提供准确轴心。
4. Blockbench 时间轴动画不会直接导入，动画参数通过交付说明提供。

## 在 CargoVerse 方块内部渲染 Create 齿轮

也可以将 Create 的齿轮作为 CargoVerse 方块的活动部件，例如机器外壳中露出半个小齿轮。

Create 已提供可复用的 PartialModel：

```
AllPartialModels.COGWHEEL
AllPartialModels.SHAFTLESS_COGWHEEL
AllPartialModels.LARGE_COGWHEEL
AllPartialModels.SHAFTLESS_LARGE_COGWHEEL
AllPartialModels.COGWHEEL_SHAFT
AllPartialModels.SHAFT_HALF
```

常见选择：

|需求|推荐模型|
|---|---|
|完整小齿轮及轴|`COGWHEEL`|
|只有小齿轮轮体|`SHAFTLESS_COGWHEEL`|
|完整大齿轮|`LARGE_COGWHEEL`|
|只有大齿轮轮体|`SHAFTLESS_LARGE_COGWHEEL`|
|独立齿轮轴|`COGWHEEL_SHAFT`|
|半截传动轴|`SHAFT_HALF`|