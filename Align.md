## Align

示例：

```dart
Container(
  height: 120.0,
  width: 120.0,
  color: Colors.blue[50],
  child: Align(
    alignment: Alignment.topRight,
    child: FlutterLogo(
      size: 60,
    ),
  ),
)
```

文档：

```dart
Align({
  Key key,
  this.alignment = Alignment.center, // 需要一个AlignmentGeometry类型的值，表示子组件在父组件中的起始位
  this.widthFactor, // 是用于确定Align 组件本身宽高的属性；它们是两个缩放因子，会分别乘以子元素的宽、高，最终的结果就是Align 组件的宽高。如果值为null，则组件的宽高将会占用尽可能多的空间。
  this.heightFactor,
  Widget child,
})
```

官方API：https://api.flutter.dev/flutter/widgets/Align-class.html