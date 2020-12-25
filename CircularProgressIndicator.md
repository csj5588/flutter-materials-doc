
## CircularProgressIndicator

示例：

```dart
CircularProgressIndicator(
  value: 0.3,
  strokeWidth: 4.0,
  backgroundColor: Color(0xffff0000),
  valueColor: new AlwaysStoppedAnimation<Color>(Colors.red),
)
```

文档：

```dart
const CircularProgressIndicator({
  Key key,
  double value ,// 0~1的浮点数，用来表示进度多少;如果 value 为 null 或空，则显示一个动画，否则显示一个定值
  Color backgroundColor, // 背景颜色
  Animation<Color> valueColor,//animation类型的参数，用来设定进度值的颜色，默认为主题色
  this.strokeWidth = 4.0,//进度条宽度
  String semanticsLabel,
  String semanticsValue,
})
```

官方API：[CircularProgressIndicator-class](https://api.flutter.dev/flutter/material/CircularProgressIndicator-class.html)