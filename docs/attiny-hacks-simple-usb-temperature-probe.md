# ATtiny Hacks:简单的 USB 温度探头

> 原文：<https://hackaday.com/2011/09/17/attiny-hacks-simple-usb-temperature-probe/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")


[Dan]的办公室非常热，但他需要一些真实的温度数据，以便向大楼管理处展示，证明开维修单是合理的。他已经在网上看到了一些简单的温度探头示例，并决定使用一个小型 AVR 芯片来构建自己的温度探头。

基于一个类似的温度监控例子 EasyLogger，他的温度探头使用 LM34 温度传感器，该传感器连接到 ATtiny45。ATtiny 使用 Ruby-USB 库和他编写的一些 Ruby 代码与他的计算机进行通信。一旦获得了数据，所有的温度测量都被记录下来，并用 RubyRRDTool 绘制成图表。

正如你在上面的图片中看到的，他的办公室比想象中要热得多，所以我们很确定他很高兴有实际的测量来支持他的说法。

如果你想自己制作一个小型温度探头，他的代码、原理图以及他在项目中使用的所有工具的链接都可以在他的网站上找到。