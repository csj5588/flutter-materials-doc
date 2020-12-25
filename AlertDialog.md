## AlertDialog

文档：

```dart
AlertDialog({
  Key key,
  this.title, /// 标题
  this.titlePadding, /// 标题padding
  this.titleTextStyle, /// 标题style
  this.content, ///内容
  this.contentPadding = const EdgeInsets.fromLTRB(24.0, 20.0, 24.0, 24.0), /// padding
  this.contentTextStyle, /// style
  this.actions,/// 动作 widget 列表,
  this.actionsPadding = EdgeInsets.zero,
  this.actionsOverflowDirection, /// action 溢出 方向
  this.actionsOverflowButtonSpacing, /// action 溢出水平间距离
  this.buttonPadding, /// 按钮padding
  this.backgroundColor, /// 背景色
  this.elevation, /// 阴影
  this.semanticLabel,
  this.insetPadding = _defaultInsetPadding,
  this.clipBehavior = Clip.none,
  this.shape,
  this.scrollable = false, /// 不可滚动,想要滚动需要嵌套SingleChildScrollView
})
```

示例：

```dart
Future<int> _getAlertDialog(BuildContext context) {
  return showDialog<int>(
  context: context,
  builder: (context) => AlertDialog(
    title: Text('Title'),
    ///如果内容过长,需要使用SingleChildScrollView
    content: Scrollbar(
      child: SingleChildScrollView(
        physics: BouncingScrollPhysics(),
        child: Text("这个是内容"),
      ),
    ),
    actions: [
      FlatButton(
        child: Text('取消'),
        onPressed: () => Navigator.of(context).pop(0),
      ),
      FlatButton(
        child: Text('确定'),
        onPressed: () => Navigator.of(context).pop(1),
      )
    ],
  ),

  ///点击dialog 外部是否消失
  barrierDismissible: true);
}
```

官方API：https://api.flutter.dev/flutter/material/AlertDialog-class.html