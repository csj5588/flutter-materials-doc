
## Image

示例：

```dart
Image(
  image: AssetImage("images/avatar.png"),
  width: 100.0,
  height: 100.0,
  color: Colors.blue, //图片的混合色值
  colorBlendMode: BlendMode.difference, // 指定混合模式
  repeat: ImageRepeat.repeatY, // 平铺 repeatY / repeatX / noRepeat
  fit: BoxFit.fill, // 缩放模式 fill / contain / cover / fitWidth / fitHeight / scaleDown / none
  alignment: Alignment.center, //对齐方式
);
```

文档：

```dart
Image(
    ImageProvider<dynamic> image;    //要显示的图像（Image()）
    String name,    //图片路径（Image.asset()）
    AssetBundle bundle,    //图片资源（Image.asset()）
    File file;    //文件路径（Image.file()）
    String src;    //图片地址url（Image.network()）
    Uint8List bytes Uint8List;    //获取的ImageStream，如sdk中从网络转Uint8List（Image.memory()）
    String semanticLabel;    //图像的语义描述
    bool excludeFromSemantics;   //是否从语义中排除此图像，默认false
    double scale;    //比例
    double width;    //宽度
    double height;   //高度
    Color color;    //颜色，如果不为null，则通过colorBlendMode属性将此颜色与图像混合
    BlendMode colorBlendMode;    //混合模式
    BoxFit fit;    //图像的显示模式
    AlignmentGeometry alignment;    //对齐方式，默认Alignment.center
    ImageRepeat repeat;    //重复方式，默认ImageRepeat.noRepeat
    Rect centerSlice;     //九宫格拉伸
    bool matchTextDirection;    //是否以文本方向绘制图片，默认false
    bool gaplessPlayback;       //当图像更改时，是继续显示旧图像（true）还是简单地显示任何内容（false），默认false
    FilterQuality filterQuality;    //筛选质量，默认FilterQuality.low
    String package, //包名（Image.asset()）
    Map<String, String> headers;    //参数可用于通过图像请求发送自定义HTTP标头（Image.network()）
)
```

官方API：[Image-class](https://api.flutter.dev/flutter/dart-ui/Image-class.html)
