## LinearProgressIndicator

示例：

```dart
LinearProgressIndicator(
  value: 0.3,
  valueColor: new AlwaysStoppedAnimation<Color>(Colors.red),
  backgroundColor: Color(0xff00ff00),
)
```

文档：

```dart
const LinearProgressIndicator({
  Key key,
  double value, // 0~1的浮点数，用来表示进度多少;如果 value 为 null 或空，则显示一个动画，否则显示一个定值
  Color backgroundColor, // 背景颜色
  Animation<Color> valueColor, // animation类型的参数，用来设定进度值的颜色，默认为主题色
  String semanticsLabel,
  String semanticsValue,
})
```

官方API：[LinearProgressIndicator-class](https://api.flutter.dev/flutter/material/LinearProgressIndicator-class.html)
