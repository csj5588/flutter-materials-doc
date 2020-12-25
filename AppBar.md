## AppBar

示例：

```dart
Widget _appBarDemo1() {
  return MaterialApp(
    debugShowCheckedModeBanner: false,
    home: Scaffold(
      appBar: AppBar(
        primary: true,//为false的时候会影响leading，actions、titile组件，导致向上偏移
        textTheme: TextTheme(//设置AppBar上面各种字体主题色
          title: TextStyle(color: Colors.red),
        ),
        actionsIconTheme: IconThemeData(color: Colors.blue,opacity: 0.6),//设置导航右边图标的主题色，此时iconTheme对于右边图标颜色会失效
        iconTheme: IconThemeData(color: Colors.black,opacity: 0.6),//设置AppBar上面Icon的主题颜色
        brightness: Brightness.dark,//设置导航条上面的状态栏显示字体颜色
        backgroundColor: Colors.amber,//设置背景颜色
        shape: CircleBorder(side: BorderSide(color: Colors.red, width: 5, style: BorderStyle.solid)),//设置appbar形状
        automaticallyImplyLeading: true,//在leading为null的时候失效
        centerTitle: true,
        title: Text('AppBar Demo'),
        leading: IconButton(
          icon: Icon(Icons.add),
          onPressed: () {
            print('add click....');
          }
        ),
        actions: <Widget>[
          IconButton(icon: Icon(Icons.search), onPressed: (){print('search....');}),
          IconButton(icon: Icon(Icons.history), onPressed: (){print('history....');}),
        ],
      ),
    ),
  );
}

```

文档：

```dart
AppBar({
  Key key,
  this.leading,//导航条左侧需要展示的Widget
  this.automaticallyImplyLeading = true,
  this.title,//导航条的标题
  this.actions,//导航条右侧要展示的一组widgets
  this.flexibleSpace,
  this.bottom,导航条底部需要展示的widget
  this.elevation,
  this.shape,//导航条样式
  this.backgroundColor,//导航条背景色
  this.brightness,//设置导航条上面的状态栏的dark、light状态
  this.iconTheme,//导航条上的图标主题
  this.actionsIconTheme,//导航条上右侧widgets主题
  this.textTheme,//导航条上文字主题
  this.primary = true,//为false的时候会影响leading，actions、titile组件，导致向上偏移
  this.centerTitle,//导航条表示是否居中展示
  this.titleSpacing = NavigationToolbar.kMiddleSpacing,
  this.toolbarOpacity = 1.0,
  this.bottomOpacity = 1.0,
})
```

官方API：[AppBar-class](https://api.flutter.dev/flutter/material/AppBar-class.html)