## TextField

示例：

```dart
TextField(
  autofocus: true, // 自动聚焦
  obscureText: false, // 是否隐藏正在编辑的文本，如用于输入密码的场景等，文本内容会用“•”替换。
  focusNode: focusNode,
  textAlign = TextAlign.start, // 输入框内编辑文本在水平方向的对齐方式。
  style: TextStyle(), // 正在编辑的文本样式
  maxLines: 1, // 输入框的最大行数，默认为1；如果为null，则无行数限制。
  maxLength: 30, // 代表输入框文本的最大长度，设置后输入框右下角会显示输入的文本计数
  maxLengthEnforced: true, // 决定当输入文本长度超过maxLength时是否阻止输入，为true时会阻止输入，为false时不会阻止输入但输入框会变红。
  onSubmitted: (ValueChanged<String> value) {}, // 输入完成回调
  onEditingComplete: () {}, // 输入完成回调
  inputFormatters: [WhitelistingTextInputFormatter(new RegExp("[a-z]"))], // 正则白名单校验 附一
  enable: false, // 是否禁用
  cursorWidth: 20.0, // 光标宽度
  cursorRadius: 
  decoration: InputDecoration(
    labelText: "用户名",
    hintText: "用户名或邮箱",
    prefixIcon: Icon(Icons.person)
  ),
),
```

文档：

```dart
TextField(
    TextEditingController controller;    // 文本编辑控制器
    FocusNode focusNode;    // 定义此窗口小部件的键盘焦点
    InputDecoration decoration;    // 在文本字段周围显示的装饰
    TextInputType keyboardType;    // 用于编辑文本的键盘类型
    TextInputAction textInputAction;    // 用于键盘的操作按钮类型
    TextCapitalization textCapitalization;    // 配置平台键盘如何选择大写或小写键盘,默认TextCapitalization.none
    TextStyle style;    // 文本样式
    StrutStyle strutStyle;    // 用于垂直布局的支柱样式
    TextAlign textAlign;    // 对齐方式,默认TextAlign.start
    TextDirection textDirection,    // 文本的方向性
    bool autofocus;    // 是否自动获取焦点,默认false
    bool obscureText;    // 是否隐藏文本（密码）,默认false
    bool autocorrect;    // 是否启用自动更正,默认true
    int maxLines;    // 最大行,默认1
    int minLines;    // 最小行
    bool expands;    // 是否将此窗口小部件的高度调整为填充其父级,默认false
    int maxLength;    // 最大长度
    bool maxLengthEnforced;    // 如果为true，则阻止该字段允许超过maxLength个 字符,默认true
    ValueChanged<String> onChanged;    // 当用户启动对TextField值的更改时调用：当他们插入或删除文本时
    VoidCallback onEditingComplete;    // 当用户提交可编辑内容时调用（例如，用户按下键盘上的“完成”按钮）
    ValueChanged<String> onSubmitted;    // 当用户指示他们已完成编辑字段中的文本时调用
    List<TextInputFormatter> inputFormatters;    // 可选的输入验证和格式覆盖
    bool enabled;    // 是否可用
    double cursorWidth;    // 光标的宽度,默认2.0
    Radius cursorRadius;    // 光标的圆角度
    Color cursorColor;    // 光标颜色
    Brightness keyboardAppearance;    // 键盘的外观
    EdgeInsets scrollPadding;    // 此值控制在滚动后TextField将位于Scrollable边缘的距离,默认EdgeInsets.all(20.0)
    DragStartBehavior dragStartBehavior;    // 确定处理拖动开始行为的方式,默认DragStartBehavior.start
    bool enableInteractiveSelection;    // 如果为true，则长按此TextField将显示剪切/复制/粘贴菜单，并且点击将移动文本插入符号
    GestureTapCallback onTap;    // 当用户点击此文本字段时调用
    InputCounterWidgetBuilder buildCounter;    // 生成自定义InputDecorator.counter小部件的回调
    ScrollPhysics scrollPhysics;    // 确定Scrollable小部件的物理特性
)
```

附一： 

- WhitelistingTextInputFormatter 白名单校验，也就是只允许输入符合规则的字符
- BlacklistingTextInputFormatter 黑名单校验，除了规定的字符其他的都可以输入
- LengthLimitingTextInputFormatter 长度限制，跟maxLength作用类似

官方API：[TextField-class](https://api.flutter.dev/flutter/material/TextField-class.html)