# 过度设计双区温度计

> 原文：<https://hackaday.com/2012/01/04/over-engineering-a-two-zone-thermometer/>

![](img/d14949ec3415946b7fe6b55c32e1659a.png "over-engineered-thermometer")

我们喜欢[Andrianakis Haris]为他的双区电子体温计增加的额外功能。由于成本增加等问题，它包含了你在大众市场商业产品上找不到的功能。例如，您可以看到 PCB 突出在 LCD 显示器上方，由于基板上钻有钥匙孔形状，因此可以将模块安装在一对螺钉上。我大大增加了董事会的规模，但在一个小的爱好运行，这通常不会影响董事会的价格取决于 fab house 定价模型。

该设计使用 ATmega8 微控制器来监控两个不同位置的传感器。有一个机载 LM35 温度传感器，用于监控该装置所在的空间。远程传感器模块使用 DHT-11 芯片来收集关于温度和湿度的数据。该传感器是有线的，但该设备有一个无线选项。可以通过可选的蓝牙模块从主板上下载数据，蓝牙模块可以焊接到主板背面的电路板上。

休息后看看视频，看看无线拉下的温度读数。[https://www.youtube.com/embed/xcWAdiAGiYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xcWAdiAGiYk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)