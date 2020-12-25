## ListView

文档：

```dart
ListView(
  IndexedWidgetBuilder itemBuilder;   //子条目布局（ListView.builder(),ListView.separated()）
  IndexedWidgetBuilder separatorBuilder;   //（ListView.separated()）
  SliverChildDelegate childrenDelegate;   //为ListView提供子代的委托（ListView.custom()）
  int itemCount;    //item数量（ListView.bu ilder(),ListView.separated()）
    List<Widget> children: const <Widget>[], //子条目布局（ListView()）
  int semanticChildCount,//子条目数量
  Axis scrollDirection: Axis.vertical;//滚动方向
  bool reverse: falsel;//是否反转滚动方向
  ScrollController controller;//滚动控制器
  bool primary;//如果为true，即使滚动视图没有足够的内容来实际滚动，滚动视图也是可滚动的。否则，默认情况下，只有具有足够内容的用户才能滚动视图，取决于physics属性
  ScrollPhysics physics;//滚动视图应如何响应用户输入
  bool shrinkWrap: false;//是否应该由正在查看的内容确定scrollDirection中滚动视图的范围
  EdgeInsetsGeometry padding;//内边距
  double itemExtent;//滚动方向上的范围
  bool addAutomaticKeepAlives: true;//是否将每个子项包装在AutomaticKeepAlive中
  bool addRepaintBoundaries: true;//是否将每个子项包装在RepaintBoundary中
  bool addSemanticIndexes: true;//是否将每个子项包装在IndexedSemantics中
  double cacheExtent;//滚动缓存区像素
  DragStartBehavior dragStartBehavior: DragStartBehavior.start;//确定处理拖动开始行为的方式
)
```

示例：

```dart
body: new Scrollbar(
  // ListView.builder写法 
  child: new ListView.builder(
    // 无分割线
    itemBuilder: (context, item) {
      return buildListData(context, titleItems[item], iconItems[item], subTitleItems[item]);
    },
    // 有分割线
    itemBuilder: (context, item) {
      return new Container(
        child: new Column(
          children: <Widget>[
            buildListData(context, titleItems[item], iconItems[item], subTitleItems[item]),
            new Divider()
          ],
        ),
      );
    },

    itemCount: iconItems.length, // 数据长度
  ),
),
```

官方API：[ListView-class](https://api.flutter.dev/flutter/widgets/ListView-class.html)