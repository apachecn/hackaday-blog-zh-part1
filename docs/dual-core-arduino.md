# 双核… Arduino？

> 原文：<https://hackaday.com/2008/04/11/dual-core-arduino/>

![](img/44b72791a450dcb448990ed00a10f3fb.png)
【约翰·瑞安】在 [Arduino 论坛](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1205243372)上发布了他的双核 Arduino 平台。这两个 ATMega168 芯片共享相同的 16Mhz 谐振器和 I2C 总线，允许它们以半并行方式运行。uC 实际上并不相互通信，但它们作为并行电路运行得相当好。这是一个非常有趣的方法，以最小的成本将 I/O 引脚添加到项目中。

*   [永久链接](http://www.arduino.cc/cgi-bin/yabb2/YaBB.pl?num=1205243372)