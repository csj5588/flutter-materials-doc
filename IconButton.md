## IconButton

文档：

```dart
IconButton(
  double iconSize: 24.0;//图标尺寸
  EdgeInsetsGeometry padding: const EdgeInsets.all(8.0);//内边距
  AlignmentGeometry alignment: Alignment.center;//对齐方式
  Widget icon;//图标控件
  Color color;//颜色
  Color highlightColor;//按钮按下时的颜色
  Color splashColor;//点击后扩散动画的颜色
  Color disabledColor;//按钮不可用时的颜色
  VoidCallback onPressed;//点击或以其他方式激活按钮时调用的回调
  String tooltip;//描述按下按钮时将发生的操作的文本
)
```

示例：

```dart
IconButton(
  icon: Icon(Icons.description),
  onPressed: () {
    print('点击了icon $index');
  },
)
```

官方API： [IconButton-class](https://api.flutter.dev/flutter/material/IconButton-class.html)