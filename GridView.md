## GridView

文档：

```dart
GridView.builder({
  Key key,
  Axis scrollDirection = Axis.vertical, // 设置滚动的方向，horizontal（水平）或vertical（垂直）
  bool reverse = false, // 是否翻转
  ScrollController controller, // 用来控制滚动位置及监听滚动事件
  bool primary,
  ScrollPhysics physics,
  bool shrinkWrap = false, // 是否根据子widget的总长度来设置GridView的长度
  EdgeInsetsGeometry padding, // 间距
  @required this.gridDelegate, // 控制子Widget如何进行布局
  @required IndexedWidgetBuilder itemBuilder,
  int itemCount,
  bool addAutomaticKeepAlives = true,
  bool addRepaintBoundaries = true,
  bool addSemanticIndexes = true,
  double cacheExtent,
  int semanticChildCount,
}) 
```

示例：

```dart
GridView(
  scrollDirection: Axis.vertical,
  gridDelegate: SliverGridDelegateWithMaxCrossAxisExtent(
    maxCrossAxisExtent: 100, // 子控件最大宽度为100
    childAspectRatio: 0.5, // 宽高比为1:2
    crossAxisSpacing: 10,
    mainAxisSpacing: 10,
  ),
  padding: EdgeInsets.all(10),
  children: List.generate(
    20,
    (index) {
      return Box(index + 1);
    },
  ),
);
```

官方API：[GridView-class](https://api.flutter.dev/flutter/widgets/GridView-class.html)