# Arduino 心率监测器

> 原文：<https://hackaday.com/2011/09/25/arduino-heart-rate-monitor/>

![](img/f3315ce414fec1cfd220e262db43bc73.png "arduino-heart-rate-monitor")

[Wolf]有一个 Polar 品牌的运动手表，可以无线监控胸带，向其发送心率数据。听起来好像有某种方法可以将手表上的数据传输到电脑上，但这只适用于 Polar 的网站。他想在设备上做更多的事情，所以他放弃了手表，并建立了一个基于 Arduino 的心率监测器。

他仍在使用胸带，并很高兴地发现 [SparkFun 为其出售 OEM 接收器](http://www.sparkfun.com/products/8660)。只需添加一个 32.768 kHz 的时钟晶体和一根可选的天线，您就可以开始运行了。一旦接收器发现一条传输胸带，它就会随着心脏的每一次跳动发出脉冲输出。[Wolf]使用 Arduino Uno 的 D2 引脚连接接收器，因为该引脚对应于 ATmega 的一个外部中断。五个输入的滚动平均值用于帮助平滑显示数据，显示在上面看到的 2.8 英寸 LCD 屏幕上。