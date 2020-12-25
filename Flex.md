## Flex

示例：

```dart
class FlexDemo extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return Flex(
      direction: Axis.horizontal,
      direction: Axis.vertical,
      children: <Widget>[
        Container(
          width: 90.0,
          height: 100.0,
          color: Colors.redAccent,
        ),
        SizedBox(width: 6,),
        Container(
          width: 90.0,
          height: 100.0,
          color: Colors.greenAccent,
        ),
        SizedBox(width: 6,),
        Container(
          width: 90.0,
          height: 100.0,
          color: Colors.blue,
        ),
        SizedBox(width: 6,),
        Container(
          width: 90.0,
          height: 100.0,
          color: Colors.orange,
        ),
      ],
    );
  }
}

```

文档：

```dart
Flex({
  Key key,
  @required this.direction,//设置flex是在水平方向上设置
  List<Widget> children = const <Widget>[],//一组子widgets
  
  <!--剩余这些定义请查看有关Row和Column的相似定义描述-->
  this.mainAxisAlignment = MainAxisAlignment.start,
  this.mainAxisSize = MainAxisSize.max,
  this.crossAxisAlignment = CrossAxisAlignment.center,
  this.textDirection,
  this.verticalDirection = VerticalDirection.down,
  this.textBaseline,
})
```

官方API：[Flex-class](https://api.flutter.dev/flutter/widgets/Flex-class.html)