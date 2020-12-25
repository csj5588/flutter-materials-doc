## TabBar

示例：

```dart
TabBar(
  onTap: (int index){
    print('Selected......$index');
  },
  unselectedLabelColor: Colors.grey, // 设置未选中时的字体颜色，tabs里面的字体样式优先级最高
  unselectedLabelStyle: TextStyle(fontSize: 20), // 设置未选中时的字体样式，tabs里面的字体样式优先级最高
  labelColor: Colors.black, // 设置选中时的字体颜色，tabs里面的字体样式优先级最高
  labelStyle: TextStyle(fontSize: 20.0), // 设置选中时的字体样式，tabs里面的字体样式优先级最高
  isScrollable: true, // 允许左右滚动
  indicatorColor: Colors.red, // 选中下划线的颜色
  indicatorSize: TabBarIndicatorSize.label, // 选中下划线的长度，label时跟文字内容长度一样，tab时跟一个Tab的长度一样
  indicatorWeight: 6.0, // 选中下划线的高度，值越大高度越高，默认为2。0
  indicator: BoxDecoration(), // 用于设定选中状态下的展示样式
  tabs: [
    Text('精选',style: TextStyle(
      color: Colors.green,
      fontSize: 16.0
    ),),
    Text('猜你喜欢',style: TextStyle(
      color: Colors.indigoAccent,
      fontSize: 16.0
    ),),
    Text('母婴'),
    Text('儿童'),
    Text('女装'),
  ]
),
```

文档：

```dart
const TabBar({
  Key key,
  @required this.tabs, // 必须实现的，设置需要展示的tabs，最少需要两个
  this.controller,
  this.isScrollable = false, // 是否需要滚动，true为需要
  this.indicatorColor, // 选中下划线的颜色
  this.indicatorWeight = 2.0, // 选中下划线的高度，值越大高度越高，默认为2
  this.indicatorPadding = EdgeInsets.zero,
  this.indicator, // 用于设定选中状态下的展示样式
  this.indicatorSize, // 选中下划线的长度，label时跟文字内容长度一样，tab时跟一个Tab的长度一样
  this.labelColor, // 设置选中时的字体颜色，tabs里面的字体样式优先级最高
  this.labelStyle, // 设置选中时的字体样式，tabs里面的字体样式优先级最高
  this.labelPadding,
  this.unselectedLabelColor, // 设置未选中时的字体颜色，tabs里面的字体样式优先级最高
  this.unselectedLabelStyle, // 设置未选中时的字体样式，tabs里面的字体样式优先级最高
  this.dragStartBehavior = DragStartBehavior.start,
  this.onTap, // 点击事件
})
```

官方API：[TabBar-class](https://api.flutter.dev/flutter/material/TabBar-class.html)