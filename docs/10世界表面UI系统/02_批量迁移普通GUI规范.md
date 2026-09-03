# 普通 GUI 向世界表面 UI 的批量迁移规范

> 已实现：可重复使用的定义、几何、渲染、装饰、命中、动作、封装仪表和集中注册骨架；装卸设备与大型货柜制造台已接入。预留：货柜机械台的业务实现。待验收：每个终端的世界模型、观察距离、多人同步和保留传统 GUI 的职责边界。

## 迁移原则

“可批量制作”表示新终端遵循固定接入路径，不表示把旧 `Screen` 自动贴到模型上。迁移前先把原界面功能分为三类：

| 内容 | 处理方式 |
| --- | --- |
| 高频状态、图标、进度、列表摘要 | 移到 `DISPLAY` 世界表面 |
| 翻页、确认、槽位切换等离散动作 | 通过同一个 `WorldUiButtonSet` 声明为显示面触摸区域或 `CONTROL` 实体按钮 |
| 文本输入、大量筛选、复杂配置、管理员维护 | 保留传统 GUI，并复用同一业务服务 |

迁移不得让世界 UI 模拟旧 Screen 点击，也不得把 Screen、Menu 或 Widget 保存到方块实体中。

## 每个终端的固定组成

一个正式终端接入至少包含：

1. 公共侧 `WorldUiDefinition`：显示表面与逻辑画布；
2. 公共侧 `WorldUiButtonSet`：统一声明触摸区域、实体按钮和各自明确的服务端动作；
3. 控制器实现 `WorldUiController`，副方块实现 `WorldUiPart`；
4. 不可变 `WorldUiViewState`：只包含当前一帧需要展示的数据；
5. 客户端 `WorldUiCanvasRenderer`：把展示快照编排为封装仪表和少量终端专用静态内容；
6. 方块实体 renderer 调用标准世界绘制入口；
7. common/client 两处集中注册；
8. 定义、几何、资源与业务动作测试。

所有成员方块统一调用 `WorldUiInteractionService.GLOBAL.dispatch(...)`，不在每个终端中重新组装全局 definition/action registry。

## 定义模板

表面职责必须显式声明，所有按钮由同一个按钮组提供：

```java
private static final WorldUiButtonSet<MyController> BUTTONS =
    createButtons();

private static final WorldUiButtonInstance CONFIRM_BUTTON =
    WorldUiButtonComponents.NORMAL.instance("confirm",
        WorldUiButtonDirection.UP);

private static WorldUiButtonSet<MyController> createButtons() {
    var builder = WorldUiButtonSet.builder(DEFINITION_ID, MyController.class);
    builder.region("detail", 128, 128, "select",
        new SurfaceRect(8, 8, 112, 24), SELECT_ACTION,
        (context, controller) -> controller.select());
    CONFIRM_BUTTON.install(builder, CONFIRM_ACTION,
        (context, controller) -> controller.confirm());
    return builder.build();
}

List<WorldUiSurfaceDefinition> surfaces = new ArrayList<>();
surfaces.add(WorldUiSurfaceDefinition.display("main", 320, 152));
surfaces.add(WorldUiSurfaceDefinition.display(
    "detail", 128, 128, BUTTONS.regions("detail")));
surfaces.addAll(BUTTONS.surfaces());

WorldUiDefinitionRegistry.GLOBAL.register(
    new WorldUiDefinition(DEFINITION_ID, surfaces));
BUTTONS.register();
```

- `DISPLAY` 自动获得共享纯色背景和向内显示框；
- `CONTROL` 不获得屏幕底色与显示框，但命中时仍由框架自动描边；
- 触摸屏仍应声明为 `DISPLAY`，交互区域不会改变表面样式职责；
- 业务终端不得手写 CONTROL 按钮表面后再单独注册动作；
- 不允许直接 `new WorldUiSurfaceDefinition(...)` 绕过显式工厂。

## 注册模板

玩法定义和动作加入公共入口：

```java
public static synchronized void bootstrap() {
    if (registered) return;
    ExampleTerminalWorldUi.bootstrap();
    registered = true;
}
```

客户端内容 renderer 加入客户端入口：

```java
ExampleTerminalRenderer.registerWorldUiRenderer();
```

禁止在方块、方块实体或 renderer 构造器中注册。构造器可能因游戏生命周期、资源重载或测试被调用多次，隐藏注册会造成顺序依赖与重复注册。

## 内容 renderer 约束

方块实体 renderer 使用标准入口：

```java
WorldUiWorldRenderer.render(
    controller.worldUiTargetSnapshot(),
    controller.worldUiViewState(),
    partialTick, poseStack, buffers, font, renderOrigin,
    packedLight, packedOverlay
);
```

画布 renderer 只处理终端内容：

- 数字、百分比、增减量、图标和状态优先复用 `client.gui.instrument` 中的封装仪表；
- 每个独立动画仪表持有自己的状态，并通过 `InstrumentStateCache` 以控制器动画键缓存；
- 正文默认调用无颜色参数的 `drawText`；
- 共享语义色取自 `CargoUiPalette`；
- 绘制深度取自 `WorldUiRenderLayers`；
- 整面填充使用 `fillCanvas`，布局边界使用 `canvasBounds`；
- 不调用背景、边框、命中解析或悬停描边 renderer；
- 不维护客户端悬停状态；
- 不每帧扫描世界寻找控制器。

禁止在终端 renderer 中复制翻转算法、频闪算法、图标扫描切换、状态灯贴图选择和仪表资源路径。确实缺少表达能力时，应先扩展或新增封装仪表，再由终端组合层调用。完整约定见[封装仪表组件规范](03_封装仪表组件规范.md)。

固定装饰顺序由框架唯一管线负责：

```text
DISPLAY 纯色背景
        ↓
终端专用内容
        ↓
DISPLAY 向内边框
        ↓
当前按钮按压脉冲
        ↓
当前 WorldUiRegion 命中描边
```

## 分批迁移顺序

建议按风险从低到高推进：

1. 纯展示或只含翻页按钮的终端；
2. 只有离散按钮、无文本输入的配置终端；
3. 需要多个表面和多方块几何的终端；
4. 装卸、交易等涉及库存与事务提交的终端；
5. 管理员输入和复杂配置继续保留传统 GUI，除非另有明确交互设计。

每次只迁移一个终端，先保留旧入口用于对照；业务和交互验收通过后再删除被完全替代的 Screen／Menu／数据同步路径。

## 单终端验收清单

- [ ] 模型实际可见区域与 `SurfaceAnchor` 一致，没有被遮挡的虚假画布；
- [ ] 画布密度符合观察距离，不直接照搬旧 GUI 尺寸；
- [ ] 六向旋转、方块接缝与多方块控制器解析正确；
- [ ] 所有交互区命中时自动描边，点中后只播放统一按钮声；
- [ ] 服务端重新进行射线、距离、区块、结构和权限检查；
- [ ] 展示快照 revision 更新后不会绘制旧状态；
- [ ] 多人同时观察与操作时状态一致；
- [ ] 传统 GUI 保留项和已删除项有明确记录；
- [ ] 可复用信息已由封装仪表表达，没有在终端内重新拼接同类视觉算法；
- [ ] 普通结构件受环境光影响，只有约定的辉光内容使用 emissive 绘制；
- [ ] common/client 集中注册与架构测试通过；
- [ ] 完整 `gradlew test` 与客户端实机验收通过。

[返回世界表面 UI 系统](README.md) · [系统架构与接入规范](01_系统架构与接入规范.md) · [封装仪表组件规范](03_封装仪表组件规范.md)
