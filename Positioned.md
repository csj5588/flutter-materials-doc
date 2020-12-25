## Positioned

示例：

```dart
Stack(
  alignment:Alignment.center ,
  fit: StackFit.expand, //未定位widget占满Stack整个空间
  children: <Widget>[
    Positioned(
      left: 18.0,
      child: Text("I am Jack"),
    ),
    Container(child: Text("Hello world",style: TextStyle(color: Colors.white)),
      color: Colors.red,
    ),
    Positioned(
      top: 18.0,
      child: Text("Your friend"),
    )
  ],
)
```

文档：

```dart
const Positioned({
  Key key,
  this.left, // 左边距 
  this.top, // 上边距
  this.right, // 右边距
  this.bottom, // 下边距
  this.width, // 需要定位元素的宽度
  this.height, // 需要定位元素的高度
  @required Widget child,
})
```

官方API：[Positioned-class](https://api.flutter.dev/flutter/widgets/Positioned-class.html)