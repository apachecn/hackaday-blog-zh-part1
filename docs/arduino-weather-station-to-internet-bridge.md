# Arduino 气象站到互联网桥

> 原文：<https://hackaday.com/2011/11/30/arduino-weather-station-to-internet-bridge/>

![](img/415fae3f2834ce909da53d0ed022469b.png "arduino-weather-station-bridge")

这个项目旨在消除将气象站数据上传到互联网所需的个人电脑。想想看，从你自己的天气感应硬件获取数据到像 Weather Underground 这样的网站根本不需要太多的处理。拼图中最大的一块是通往互联网的窗口，这可以用微控制器而不是永远在线的计算机轻松完成。

在这种情况下，[Boris Landoni]使用 Arduino 以及 RS232 屏蔽和以太网屏蔽。气象站，一个拉克罗斯 WS23xx 系列，已经有一个 RS232 串行端口来获取数据。屏蔽是必要的，以逐步降低电压的水平，将发挥 Arduino 很好。它还为您提供了一个 D-Sub 连接器，便于连接。从那里，他开始研究气象地下应用编程接口的文档，编写代码来构建必要的字符串，这些字符串以固定的间隔通过以太网连接发送出去。

如果你的气象站只提供了一个 USB 接口，你还不算倒霉。[使用具有 USB 主机](http://hackaday.com/2011/10/21/extend-your-personal-weather-stations-reporting-capabilities/)功能的嵌入式平台，您可以获得与我们在这里看到的相同的结果。