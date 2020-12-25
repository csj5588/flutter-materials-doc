## Column

示例：

```dart
Column(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  crossAxisAlignment: CrossAxisAlignment.center,
  textBaseline: TextBaseline.ideographic,
  textDirection: TextDirection.rtl,
  verticalDirection: VerticalDirection.up,
  children: <Widget>[
    Icon(Icons.opacity),
    Icon(Icons.settings),
    Container(
      color: Colors.redAccent,
      width: 100.0,
      height: 100.0,
      child: Text('data'),
    ),
    Icon(Icons.ondemand_video),
  ],
)
```

文档：

```dart
Column({
  Key key,
  MainAxisAlignment mainAxisAlignment = MainAxisAlignment.start,//子Widget在纵轴上的排列，全部子Widget从顶部开始展示
  MainAxisAlignment.end//子Widget在纵轴上的排列，全部子Widget挨着底部展示
  MainAxisAlignment.center//子Widget在纵轴上的排列，全部子widget在中间展示
  MainAxisAlignment.spaceBetween//子Widget在纵轴上的排列，两两子widget之间间距相等，最上最下子widget挨着边展示
  MainAxisAlignment.spaceAround//子Widget在纵轴上的排列，两两子widget之间间距相等，最上最下子widget离边的距离为两两子widget之间距离的一半
  MainAxisAlignment.spaceAround//子Widget在纵轴上的排列，两两子widget之间间距相等，最上最下子widget离边的距离为两两子widget之间距离相等
  MainAxisSize mainAxisSize = MainAxisSize.max,//设置Column占据的空间为最大
  CrossAxisAlignment crossAxisAlignment = CrossAxisAlignment.start,//设置全部子widget左边对齐
  CrossAxisAlignment.end//设置全部子widget右边对齐
  CrossAxisAlignment.stretch//设置全部子widget占据整个横轴（X）方向，拉伸对齐Column左右两边
  CrossAxisAlignment.baseline,//相当于CrossAxisAlignment.start,但是需要配合textBaseline，不然会报错
  TextDirection textDirection,//设置子widget的左右显示方位，只有在crossAxisAlignment为start、end的时候起作用；
  VerticalDirection verticalDirection = VerticalDirection.down,//设置子Widget在纵轴（Y）的起始位置，down表示，第一个widget从开始位置展示，后面的跟着依次展示；相当于正序
  VerticalDirection.up//表示第一个widget从末尾位置开始展示，后面的跟着依次展示，相当于倒序
  TextBaseline textBaseline,//配合CrossAxisAlignment.baseline一起使用
  List<Widget> children = const <Widget>[],//装在一组子widgets
})
```

官方API：[Column-class](https://api.flutter.dev/flutter/widgets/Column-class.html)