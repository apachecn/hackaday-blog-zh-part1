# ATtiny Hacks:读取摩托车的 J1850 数据总线

> 原文：<https://hackaday.com/2011/09/19/attiny-hacks-reading-from-a-motorcycles-j1850-data-bus/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")


[TZ]一直在使用 ATtiny 微控制器读取和传递来自他的哈雷戴维森摩托车的数据。你在上面看到的图像是[使用 ATtiny 4313 从 J1850 总线](http://www.youtube.com/watch?v=P3BzX0D8vuc)读取数据。

[J1850 协议](http://www.interfacebus.com/Automotive_SAE_J1850_Bus.html)是一个较旧的标准，可能不适用于较新的车辆。但是如果你的车上有，你可以通过一个 ODB-II 连接器接入总线。[TZ]正在用 4313 解码数据，然后使用廉价的蓝牙模块将信息发送到 Android 平板电脑上。幸运的是，已经有人编写了一个漂亮的 GUI 来显示速度和转速表。

这不是他探索的用 ATtiny 芯片收集数据的唯一方法。广告之后的第二段视频展示了一个更复杂的设置。它仍然以同样的方式收集 J1850 数据，但也使用额外的 I2C 传感器和嵌入式 ARM 板来收集 GPS 数据。一切都被推送到他的智能手机上，智能手机通过 WiFi 连接显示当前的档位、转速、速度、发动机温度、燃油油位和 GPS 信息。

[https://www.youtube.com/embed/P3BzX0D8vuc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/P3BzX0D8vuc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/Td34w0LIyOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Td34w0LIyOU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)