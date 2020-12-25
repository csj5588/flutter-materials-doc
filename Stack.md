## Stack

示例：

```dart
Stack(
  alignment: AlignmentDirectional.center,
  textDirection: TextDirection.rtl,
  fit: StackFit.passthrough,
  children: <Widget>[
    Container(
      color: Colors.redAccent,
      width: 100.0,
      height: 100.0,
      child: Text('data'),
    ),
    Icon(Icons.settings),
    Positioned(
      top: 10,
      left: 60,
      child: Icon(Icons.settings)
    ),
    Icon(Icons.opacity),
    Icon(Icons.ondemand_video),
  ],
)

```

文档：

```dart
Stack({
  Key key,
  this.alignment = AlignmentDirectional.topStart,//设置子Widget开始展示的位置，从顶部开始展示
  AlignmentDirectional.topCenter//从顶部中间开始展示
  AlignmentDirectional.topEnd//从顶部结束位置展示
  AlignmentDirectional.centerStart//从中间开始位置开始展示
  AlignmentDirectional.center//从正中间展示
  AlignmentDirectional.centerEnd//从中间结束位置展示
  AlignmentDirectional.bottomStart//从底部开始位置展示
  AlignmentDirectional.bottomCenter//从底部中间位置展示
  AlignmentDirectional.bottomEnd//从底部结束位置展示
  this.textDirection,//设置子widget的左右显示方位
  this.fit = StackFit.loose,//设置没有通过positioned包裹的子widget的size，loose表示，以他子widget最大的size展示
  StackFit.expand//stack的size等于他父widget的size
  this.overflow = Overflow.clip,子widget超出stack时的截取方式，参考Text的溢出截取方式
  List<Widget> children = const <Widget>[],//一组子widgets
})

```

官方文档：[Stack-class](https://api.flutter.dev/flutter/widgets/Stack-class.html)