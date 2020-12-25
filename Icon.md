
## Icon

示例：

```dart
String icons = "";
// accessible: &#xE914; or 0xE914 or E914
icons += "\uE914";
// error: &#xE000; or 0xE000 or E000
icons += " \uE000";
// fingerprint: &#xE90D; or 0xE90D or E90D
icons += " \uE90D";


Text(icons,
  style: TextStyle(
      fontFamily: "MaterialIcons",
      fontSize: 24.0,
      color: Colors.green
  ),
);
```

```dart
Icon(
  IconData icon;//系统库中的图标文件
  double size;//图标的尺寸
  Color color;//绘制图标时使用的颜色
  String semanticLabel;//图标的语义标签
  TextDirection textDirection;//用于渲染图标的文本方向
)
```

官方图标库：[material-icons](https://material.io/tools/icons/)
文档：[Icon-class](https://api.flutter.dev/flutter/widgets/Icon-class.html)
