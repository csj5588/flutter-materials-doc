## Text

示例：

```dart
Text("Hello world",
  style: TextStyle(
    color: Colors.blue,
    fontSize: 18.0,
    height: 1.2,  
    fontFamily: "Courier",
    fontWeight: FontWeight.bold,
    fontStyle: FontStyle.italic,
    background: new Paint()..color=Colors.yellow,
    decoration: TextDecoration.underline,
    decorationStyle: TextDecorationStyle.dashed,
  ),
  textAlign: TextAlign.center,
  overflow: TextOverflow.ellipsis,
  maxLines: 1,
);
```

文档：

```dart
Text(
    String data;    // 文本内容（Text()）
    TextSpan textSpan; // 文本内容（Text.rich()）
    TextStyle style;     // 文本样式
    StrutStyle strutStyle;    // 段落样式
    TextAlign textAlign;    // 本文对其方式
    TextDirection textDirection;    // 文本方向
    Locale locale;    // 选择区域特定字形的语言环境
    bool softWrap;     // 是否自动换行
    TextOverflow overflow;    // 如何处理文本溢出
    double textScaleFactor;    // 每个逻辑像素的字体像素数
    int maxLines;    // 文本的最大行数，如果文本超过给定的行数，则会根据overflow字段截断
    String semanticsLabel;    // 文本的替代语义标签
)
```

官方API: [Text-class](https://api.flutter.dev/flutter/widgets/Text-class.html)