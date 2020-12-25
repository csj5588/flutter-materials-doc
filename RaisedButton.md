## RaisedButton

文档：

```dart
RaisedButton(
    requiredVoidCallback onPressed;  //点击或以其他方式激活按钮时调用的回调
    ValueChanged<bool> onHighlightChanged;  //由底层InkWell小部件的InkWell.onHighlightChanged 回调调用
    ButtonTextTheme textTheme;  //文本主题
    Color textColor;  //文本颜色
    Color disabledTextColor;  //按钮不可用时的文本颜色
    Color color;  //按钮颜色
    Color disabledColor;   //按钮不可用时的颜色
    Color highlightColor;  //按钮按下时的颜色
    Color splashColor;     //点击后扩散动画的颜色
    Brightness colorBrightness;  //用于此按钮的主题亮度
    double elevation;  //凸出的高度
    double highlightElevation;  //按下按钮时凸出的高度
    double disabledElevation;  //按钮不可用时凸出的高度
    EdgeInsetsGeometry padding;  //内边距
    ShapeBorder shape;  //按钮材质的形状
    Clip clipBehavior: Clip.none;  //剪裁
    MaterialTapTargetSize materialTapTargetSize;  //配置点击目标的最小尺寸
    Duration animationDuration;  //动画的持续时间
    Widget child;  //子控件（RaisedButton()）
    Widget icon;  //图标（RaisedButton.icon()）
    Widget label;//文本（RaisedButton.icon()）
)
```

示例：

```dart
RaisedButton(
  onPressed: () {},
  child: Text("textColor文本的颜色，color背景颜色，highlightColor按钮按下的颜色"),
  textColor: Color(0xffff0000),
  color: Color(0xfff1f1f1),
  highlightColor: Color(0xff00ff00),
)
```

官方API：[RaisedButton-class](https://api.flutter.dev/flutter/material/RaisedButton-class.html)