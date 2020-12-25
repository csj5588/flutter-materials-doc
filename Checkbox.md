
## Checkbox

示例：

```dart
new Checkbox(
  value: this.check,
  tristate: true, // 如果为 true，那么复选框的值可以是 true，false 或 null。
  autofocus: true, // 当前作用域中的初始焦点
  activeColor: Colors.blue, // 激活时的颜色
  focusColor: Colors.blue, // 聚焦时的颜色
  checkColor: Colors.blue, // 选中图标的颜色
  hoverColor: Colors.blue, // hover时的颜色
  materialTapTargetSize: MaterialTapTargetSize.padded // 配置tap目标的最小大小, 点击区域尺寸，padded：向四周扩展48px区域 shrinkWrap：控件区域
  focusNode: focusNode,
  onChanged: (bool val) {
    this.setState(() {
        this.check = !this.check;
    });
  },
),
```

官方文档：[Checkbox-class](https://api.flutter.dev/flutter/material/Checkbox-class.html)