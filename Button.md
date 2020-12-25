
## Button

示例：

```dart
FlatButton(
  color: Colors.blue,
  textColor: Colors.white,  // 按钮文字颜色
  highlightColor: Colors.blue[700], // 点击时，水波动画中水波的颜色
  disabledTextColor: Colors.gray,  //按钮禁用时的文字颜色
  colorBrightness: Brightness.dark,  // 按钮主题，默认浅色主题
  splashColor: Colors.grey,
  padding:    // 按钮的填充
  shape:RoundedRectangleBorder(borderRadius: BorderRadius.circular(20.0)), // 外形
  child: Text("Submit"),
  onPressed: () {},
)
```

官方API： [FlatButton-class](https://api.flutter.dev/flutter/material/FlatButton-class.html)
