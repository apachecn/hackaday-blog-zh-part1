# 用便宜的安卓系统控制可爱的宜家小夜灯

> 原文：<https://hackaday.com/2012/01/19/controlling-a-cute-ikea-night-light-with-android-on-the-cheap/>

![](img/9488625fc46c93c9e03ae7b9284af48d.png "LED")

当[trandi]的妻子在宜家看到可爱的小夜灯时，她必须拥有它。她实际上买了几个，因为她的丈夫不可避免地会打开一个，开始摆弄里面的微控制器。不可避免的攻击很酷，也给了我们一些与 Android 廉价接口的想法。

这座建筑最初是一盏宜家的 Spoka 夜灯，一盏可爱的拟人化夜灯，有着柔软的硅胶外壳。Spoka 内部有十几个三色发光二极管，[trandi]只需按一下按钮就可以循环显示。在决定用安卓手机控制 Spoka 内部的灯光后，他伸手去拿一个 [IOIO](http://www.sparkfun.com/products/10748) 安卓分线板。命运干涉了，[trandi]最终得到了一个[便宜得离谱的蓝牙模块](http://www.goodluckbuy.com/serial-bluetooth-rf-transceiver-module-rs232.html)，它提供了与其他蓝牙设备的简单串行连接。

该建筑在夜间照明中重复使用蓝色、红色、橙色的 led，但用 ATtiny2313 取代了没有名字的 8 引脚微处理器。[Trandi]编写了一个小的 Android 应用程序，通过蓝牙串行连接来控制颜色。休息之后看看他的演示。

[https://www.youtube.com/embed/C9aHQkkmqHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C9aHQkkmqHI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)