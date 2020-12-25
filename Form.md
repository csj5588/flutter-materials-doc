## Form

示例：

```dart
Form(
  key: _formKey, // 设置globalKey，用于后面获取FormState
  autovalidate: true, // 开启自动校验
  onWillPop: Future .. , // 异步拦截路由返回。
  onChanged: (v) {
    print("onChange: $v");
  }
  child: ...
)
```

##  FormField

示例：

```dart
TextFormField(
  decoration: InputDecoration(
    hintText: '电话号码',
  ),
  validator: (value) {
    RegExp reg = new RegExp(r'^\d{11}$');
    if (!reg.hasMatch(value)) {
      return '请输入11位手机号码';
    }
    return null;
  },
)
```

文档：

```dart
const FormField({
  ...
  FormFieldSetter<T> onSaved, //保存回调
  FormFieldValidator<T>  validator, //验证回调
  T initialValue, //初始值
  bool autovalidate = false, //是否自动校验。
})
```

官方API：[Form-class](https://api.flutter.dev/flutter/widgets/Form-class.html)