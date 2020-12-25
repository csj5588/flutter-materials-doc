
## Switch

示例 + 文档：

```dart
new Switch(
  value: this.check, // bool 切换按钮的值。
  activeColor: Colors.blue,     // 激活时原点颜色
  activeThumbImage: ImageProvider, // 图片激活时的效果。
  activeTrackColor: Colors.blue,   // 激活时横条的颜色。
  inactiveThumbColor: Colors.black, // 非激活时原点的颜色
  inactiveThumbImage: ImageProvider, // 非激活原点的图片效果。
  inactiveTrackColor: Colors.black, // 非激活时横条的颜色。
  onChanged: (bool val) {
    this.setState(() {
      this.check = !this.check;
    });
  },
)
```

官网API： [Switch-class](https://api.flutter.dev/flutter/material/Switch-class.html)
