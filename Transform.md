## Transform

示例：

```dart
Container(
  color: Colors.black,
  child: new Transform(
    alignment: Alignment.topRight, // 相对于坐标系原点的对齐方式
    transform: new Matrix4.skewY(0.3), // 沿Y轴倾斜0.3弧度
    child: new Container(
      padding: const EdgeInsets.all(8.0),
      color: Colors.deepOrange,
      child: const Text('Apartment for rent!'),
    ),
  ),
);
```

平移：

```dart
DecoratedBox(
  decoration:BoxDecoration(color: Colors.red),
  // 默认原点为左上角，左移20像素，向上平移5像素  
  child: Transform.translate(
    offset: Offset(-20.0, -5.0),
    child: Text("Hello world"),
  ),
)
```

旋转：

```dart
DecoratedBox(
  decoration:BoxDecoration(color: Colors.red),
  child: Transform.rotate(
    // 旋转90度
    angle: math.pi/2 ,
    child: Text("Hello world"),
  ),
)；
```

缩放：

```dart
DecoratedBox(
  decoration:BoxDecoration(color: Colors.red),
  child: Transform.scale(
      scale: 1.5, // 放大到1.5倍
      child: Text("Hello world")
  )
);
```

layout 旋转：

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.center,
  children: <Widget>[
    DecoratedBox(
      decoration: BoxDecoration(color: Colors.red),
      // 将Transform.rotate换成RotatedBox  
      child: RotatedBox(
        quarterTurns: 1, // 旋转90度(1/4圈)
        child: Text("Hello world"),
      ),
    ),
    Text("你好", style: TextStyle(color: Colors.green, fontSize: 18.0),)
  ],
),
```

官方API：[Transform-class](https://api.flutter.dev/flutter/widgets/Transform-class.html)