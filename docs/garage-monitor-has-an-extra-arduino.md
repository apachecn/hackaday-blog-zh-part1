# 车库监视器有一个额外的 Arduino

> 原文：<https://hackaday.com/2010/12/14/garage-monitor-has-an-extra-arduino/>

![](img/b6abb3568516aff9e81502d0a9812fb5.png "Arduino_Garage_Door_Sensor-2")

[Jody]想知道他的车库门什么时候开。他详细介绍了他的设置，该设置使用 Arduino 读取的温度传感器通过 XBee 无线电发送到运行 Windows 服务的计算机。我们[在](http://hackaday.com/?s=%22garage+door+indicator%22)之前已经见过两次了，这是值得注意的教训。XBee 无线电能够读取模拟数据、中继数字信号等等。这意味着 Arduino 是完全不必要的。例如， [Tweet-a-Watt](http://hackaday.com/2009/01/24/wattcher-twittering-kill-a-watt-plans-posted/) 使用 XBee 的两个 ADC 来测量 Kill-a-Watt 功率计中的电压和电流。在 [SparkFun](http://www.sparkfun.com/tutorials/122) 和 [Adafruit](http://ladyada.net/make/xbee/usermanual.html) 教程的帮助下，编写 XBee 真的很简单。一点编程和焊接应该能让 Jody 拿回他的 Arduino。我们希望这篇笔记能帮助你找到 XBees 在没有微控制器的情况下的更多创造性用途。

[通过[使](http://blog.makezine.com/archive/2010/11/garage_status_monitor.html)