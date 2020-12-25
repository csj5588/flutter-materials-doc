## Scaffold

继承关系
Object > Diagnosticable > DiagnosticableTree > Widget > StatefulWidget > Scaffold

实现基本设计视觉布局结构。支撑整个界面的内容，也是继承于Widget,一个控件。

文档:

```dart
Scaffold({
  Key: key,
  PreferredSizeWidget: appBar, // 一个设计应用程序栏。
  Widget Body, // 内容控件
  Widget floatingActionButton, // 浮动按钮FloatingActionButton
  FloatingActionButtonLocation floatingActionButtonLocation.endFloat， // 浮动按钮放置的位置 centerFloat | endDocked | centerDocked | endFloat，
  FloatingActionButtonAnimator floatingActionButtonAnimator, // 浮动按钮动画：FloatingActionButtonAnimator.scaling
  List<Widget> persistentFooterButtons, // 底部控件二
  Widget Drawer, // 左滑布局 ,主动调用： Scaffold.of(context).openDrawer();
  Widget endDrawer, // 右滑布局 ,主动调用： Scaffold.of(context).openEndDrawer();
  Widget bottomNavigationBar, // 底部控件三
  Widget bottomSheet, // 底部控件一
  Color backgroundColor, // 背景颜色
  bool resizeToAvoidBottomPadding = true, // 是否调整主体的大小以避免键盘遮挡部分布局
  bool primary = true, // 是否填充顶部（状态栏）
})
```

示例：

```dart
Scaffold(
  appBar: AppBar(
    leading: null,
    automaticallyImplyLeading: false,
    title: Text(widget.title),
    actions: <Widget>[
      IconButton(
        icon: Icon(Icons.ac_unit),
        onPressed: () {},
      ),
      new PopupMenuButton<String>(
        itemBuilder: (BuildContext context) => <PopupMenuItem<String>>[
          new PopupMenuItem(child: new Text("我的")),
          new PopupMenuItem(child: new Text("设置")),
          new PopupMenuItem(child: new Text("钱包")),
        ]
      )
    ],
    elevation: 10,
    shape: new RoundedRectangleBorder(borderRadius: BorderRadius.circular(10.0),side: new BorderSide(
      style: BorderStyle.none,
    )),
    backgroundColor:Colors.green,
    brightness: Brightness.light,
    iconTheme: IconTheme.of(context).copyWith(color: Colors.black),
    actionsIconTheme: IconTheme.of(context).copyWith(color: Colors.black),
    textTheme: Theme.of(context).textTheme.apply(fontSizeFactor: 1.2),
    primary: true,
    centerTitle: true,
    titleSpacing: 10,
    toolbarOpacity: 1.0,
    bottomOpacity : 0.5,
  ),
  body: Center(
    child: Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: <Widget>[
        Text(
          'Hello Flutter',
        ),
      ],
    ),
  ),
  floatingActionButton: FloatingActionButton(
    child: Icon(Icons.add),
    tooltip: 'Increment',
    foregroundColor: Colors.cyanAccent,
    backgroundColor: Colors.green,
    focusColor: Colors.red,
    hoverColor: Colors.black,
    onPressed: _showMessage,
    shape :const CircleBorder(),
    clipBehavior: Clip.none,
    focusNode: _node,
    isExtended: true,
  ),
  floatingActionButtonLocation: FloatingActionButtonLocation.centerFloat,
  floatingActionButtonAnimator: FloatingActionButtonAnimator.scaling,
  persistentFooterButtons: <Widget>[
    Text('取消'),
    Text('确定')
  ],
  drawer: new Drawer(
    child: new UserAccountsDrawerHeader(
      accountName: new Text(
        "Flutter",
      ),
      accountEmail: new Text(
        "Flutter@gmail.com",
      ),
    ),
  ),
  bottomNavigationBar:BottomNavigationBar(
    items:[
        BottomNavigationBarItem(
          icon: Icon(Icons.home),
          title: Text(
            '首页',
          ),
        ),
        BottomNavigationBarItem(
          icon: Icon(Icons.home),
          title: Text(
            '社区',
          ),
        ),
        BottomNavigationBarItem(
          icon: Icon(Icons.home),
          title: Text(
            '我的',
          ),
        ),
    ],
    currentIndex:0,
  ),
  bottomSheet: Text('底部弹出框'),
  primary: true,
  drawerDragStartBehavior: DragStartBehavior.down,
  extendBody: true,
  drawerScrimColor: Color.fromARGB(50, 0, 0, 0),
);
```

官方API：[Scaffold-class](https://api.flutter.dev/flutter/material/Scaffold-class.html)