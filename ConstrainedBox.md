## ConstrainedBox

尺寸限制类容器

示例：

```dart
ConstrainedBox(
  constraints: BoxConstraints(
    this.minWidth = 0.0, //最小宽度
    this.maxWidth = double.infinity, //最大宽度
    this.minHeight = 0.0, //最小高度
    this.maxHeight = double.infinity //最大高度
  ),
  child: Container(
      height: 5.0, 
      child: redBox 
  ),
)
```

官方API：[ConstrainedBox-class](https://api.flutter.dev/flutter/widgets/ConstrainedBox-class.html)