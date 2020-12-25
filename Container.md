## Container

容器

示例：

```dart
Container(
  alignment: Alignment.center,//child子Widget距中展示
  padding: EdgeInsets.all(20),//设置Container的内边距为20.0
  margin: EdgeInsets.all(20.0),//设置Container的外边距为20.0
  color: Colors.black,//设置背景色为黑色
  width: 200.0,//设置宽度为200.0
  height: 200.0,//设置高度为200.0
  child: Text(//child填充为Text
    '这是一个Container',//显示文字
    textDirection: TextDirection.ltr,//文字从左到右显示
    style: TextStyle(//Text样式
    color: Colors.redAccent,//文字颜色
    backgroundColor: Colors.black,//Text背景色
  ),),
)

```

文档：

```dart
Container({
  Key key,
  this.alignment,//Alignment,设置Container里面child的对齐方式
  this.padding,//EdgeInsets,设置内边距
  Color color,//设置Container的背景色
  Decoration decoration,//设置Container的child后面的装饰
  this.foregroundDecoration,// 设置Container的child前面的装饰
  double width,//设置Container的宽度
  double height,//设置Container的高度
  BoxConstraints constraints,//设置Container的子元素约束
  this.margin,//EdgeInsets，设置外边距
  this.transform,//设置Container的转换矩阵
  this.child,//Widget，设置Container的child
}

```

官方API：[Container-class](https://api.flutter.dev/flutter/widgets/Container-class.html)