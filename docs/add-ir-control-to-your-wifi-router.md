# 为您的 WiFi 路由器添加红外控制

> 原文：<https://hackaday.com/2009/09/29/add-ir-control-to-your-wifi-router/>

![wrt54g_ir_receiver](img/0367d52f16eda849dc452a01f1ff7824.png "wrt54g_ir_receiver")

[Craig]想在他的电视上使用 [Boxee](http://www.boxee.tv) ，但是他的电脑在另一个房间。他设计了一种相当[可疑的方法来传送音频/视频信号](http://hackingwithgum.com/2009/06/01/building-a-boxee-tv-station/)(这是一种最喉音意义上的黑客行为)。对我们来说更有趣的是[他的遥控界面](http://hackingwithgum.com/2009/09/28/building-a-boxee-remote-control/)解决方案。我们熟悉构建 [USB 连接的红外接收器](http://hackaday.com/2008/10/30/how-to-usb-remote-control-receiver/)，但【Craig】决定在他的 Linksys WRT54G 路由器的串行连接中插入一个。

令人惊讶的是，路由器外壳中有很大的空间来添加更多的电子设备。他将一个 7805 电压调节器连接到路由器的 12v 电源上，并用它来为一个 IR 接收器模块和一个 ATmega328 供电。因为路由器的串行端口需要 3.3v 电压，所以他使用齐纳二极管和电阻来降低通信电压。通过加载 [Tomato](http://www.polarcloud.com/tomato) 作为路由器固件，远程控制信号可以被传送回主机上运行的 python 脚本。

我们确实对可能的改进有一些意见。使用 ATmega328 大约是 30kB 的过度使用。我们知道[基于软件的 usb 红外接收器](http://jumptuck.wordpress.com/2008/10/26/usb-ir-receiver/)运行在不到 2 千字节的编程空间上。此外，所用的 IR 接收器模块(TSOP1738)已经过时。这种情况下，我们可能会推荐 TSOP34138。换成这款器件并使用低功耗 AVR，您应该能够使用路由器的 3.3v 稳压电源。这将消除额外的调节器，并防止路由器机箱内增加更多热量。

但是撇开硬件选择的争论不谈，我们喜欢这个解决方案的创造性。干得好！