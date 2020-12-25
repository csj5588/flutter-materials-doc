## Wrap

示例：

```dart
class WrapDemo extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    // TODO: implement build
    return  Wrap(
      direction: Axis.vertical,
      direction: Axis.horizontal,
      spacing: 16.0, // 在direction: Axis.horizontal的时候指左右两个Widget的间距,在direction: Axis.vertical的时候指上下两个widget的间距
      runSpacing: 16.0,// 在direction: Axis.horizontal的时候指上下两个Widget的间距,在direction: Axis.vertical的时候指左右两个widget的间距
      alignment: WrapAlignment.start,
      crossAxisAlignment: WrapCrossAlignment.start,
      textDirection: TextDirection.ltr,
      verticalDirection: VerticalDirection.up,
      children: <Widget>[
        ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
          color: Colors.orange,
            child: Text('历史记录1'),
          ),
        ),
        ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
            color: Colors.redAccent,
            child: Text('历史记录2'),
          ),
        ),
        ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
            color: Colors.blue,
            child: Text('历史记录3'),
          ),
        ),
        ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
            color: Colors.greenAccent,
            child: Text('历史记录4'),
          ),
        ),
         ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
            color: Colors.amber,
            child: Text('历史记录5'),
          ),
        ),
        ClipRRect(
          borderRadius: BorderRadius.circular(10.0),
          child: Container(
            alignment: Alignment.center,
            width: 86.0,
            height: 36.0,
            color: Colors.indigoAccent,
            child: Text('历史记录6'),
          ),
        ),
      ],
    );
  }
}

```

文档：

```dart
Wrap({
  Key key,
  this.direction = Axis.horizontal, // 设置水平局部还是垂直布局
  this.alignment = WrapAlignment.start, // 设置元素的其实位置，
  
  this.spacing = 0.0, // 在direction: Axis.horizontal的时候指左右两个Widget的间距,在direction: Axis.vertical的时候指上下两个widget的间距
  this.runAlignment = WrapAlignment.start, // 设置widget与widget在水平或者垂直轴上的间距
  WrapAlignment.start // 每一行（列）子Widget在纵（横）轴上的排列，全部子Widget从顶部开始展示
  WrapAlignment.end // 每一行（列）子Widget在纵（横）轴上的排列，全部子Widget挨着底部展示
  WrapAlignment.center // 每一行（列）子Widget在纵（横）轴上的排列，全部子widget在中间展示
  WrapAlignment.spaceBetween // 每一行（列）子Widget在纵（横）轴上的排列，两两子widget之间间距相等，最上最下子widget挨着边展示
  WrapAlignment.spaceAround // 每一行（列）子Widget在纵（横）轴上的排列，两两子widget之间间距相等，最上最下子widget离边的距离为两两子widget之间距离的一半
  WrapAlignment.spaceAround // 每一行（列）子Widget在纵（横）轴上的排列，两两子widget之间间距相等，最上最下子widget离边的距离为两两子widget之间距离相等
  this.runSpacing = 0.0, // 在direction: Axis.horizontal的时候指上下两个Widget的间距,在direction: Axis.vertical的时候指左右两个widget的间距
  this.crossAxisAlignment = WrapCrossAlignment.start, // 水平排列时控制全部子widgets的上部对齐，垂直排列时控制全部子widgets的左边对齐
  WrapCrossAlignment.end // 水平排列时控制全部子widgets的下部对齐，垂直排列时控制全部子widgets的又边对齐
  WrapCrossAlignment.center // 设置每一行的子Widgets剧中对齐
  this.textDirection, // 设置每一行（列）的展示 
  textDirection: TextDirection.ltr // 设置每一行（列）的子Widgets从左到右（从上到下）正常显示，正序排列
  textDirection: TextDirection.rtl // 设置每一行（列）的子Widgets倒序显示
  this.verticalDirection = VerticalDirection.down, // 设置行列widgets的展示，正常显示
  VerticalDirection.up // 倒序展示，比如，在direction: Axis.horizontal时有1、2、3行widgets，设置为up后，展示为3、2、1  
  List<Widget> children = const <Widget>[], // 一组子widgets
})

```

官方API：[Wrap-class](https://api.flutter.dev/flutter/widgets/Wrap-class.html)