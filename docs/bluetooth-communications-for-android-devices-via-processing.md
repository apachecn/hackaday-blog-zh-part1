# 通过处理实现 Android 设备的蓝牙通信

> 原文：<https://hackaday.com/2011/09/26/bluetooth-communications-for-android-devices-via-processing/>

![](img/bdb16eae7b48d5638a158f5996d196b0.png "bluetooth-for-android-processing")

[Oscar]向我们展示了如何使用[一个 Android 的处理草图与蓝牙设备](http://webdelcire.com/wordpress/archives/1045) ( [翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwebdelcire.com%2Fwordpress%2Farchives%2F1045))进行通信。事实证明这比你想象的要简单。Processing 和 Android 都与 Java 密切相关，您可以在 Processing sketch 中导入处理蓝牙的 Android 库。这使得启动草图时可以轻松启用蓝牙调制解调器，并管理与设备的连接以及发送和接收数据。

在本例中，[Oscar]使用带有蓝牙模块的 Arduino 作为测试设备。他的草图首先显示哪些设备可用，然后连接到您从列表中选择的设备。11 行 Arduino 代码通过串行端口传输一个值，并监听命令以切换引脚 13 上的 LED。[Oscar]在他的教程中花时间向我们展示了处理草图的每个步骤是如何组装的，而不仅仅是发布完成的代码。

[谢谢莎拉]