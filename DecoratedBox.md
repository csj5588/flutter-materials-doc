## DecoratedBox

DecoratedBox可以在其子组件绘制前(或后)绘制一些装饰（Decoration），如背景、边框、渐变等

示例：

```dart
DecoratedBox(
  decoration: BoxDecoration(
    gradient: LinearGradient(colors:[Colors.red,Colors.orange[700]]), //背景渐变
    borderRadius: BorderRadius.circular(3.0), //3像素圆角
    boxShadow: [ //阴影
      BoxShadow(
        color:Colors.black54,
        offset: Offset(2.0,2.0),
        blurRadius: 4.0
      )
    ]
  ),
  child: Padding(padding: EdgeInsets.symmetric(horizontal: 80.0, vertical: 18.0),
    child: Text("Login", style: TextStyle(color: Colors.white),),
  )
)
```

文档：

```dart
const DecoratedBox({
  Decoration decoration, // 代表将要绘制的装饰，它的类型为Decoration
  DecorationPosition position = DecorationPosition.background, // background 背景装饰 ｜ foreground 前景装饰
  Widget child
})

BoxDecoration({
  Color color, //颜色
  DecorationImage image,//图片
  BoxBorder border, //边框
  BorderRadiusGeometry borderRadius, //圆角
  List<BoxShadow> boxShadow, //阴影,可以指定多个
  Gradient gradient, //渐变
  BlendMode backgroundBlendMode, //背景混合模式
  BoxShape shape = BoxShape.rectangle, //形状
})
```

官方API：[DecoratedBox-class](https://api.flutter.dev/flutter/widgets/DecoratedBox-class.html)