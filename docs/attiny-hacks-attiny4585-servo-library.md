# ATtiny Hacks: ATtiny45/85 伺服库

> 原文：<https://hackaday.com/2011/09/25/attiny-hacks-attiny4585-servo-library/>

![ATtiny Hacks Theme Banner](img/5f674cf2d4b94faba5f6b413d805f657.png "ATtiny Hacks Theme Banner")

![](img/4346764b55866bf3eb988b7176604aa5.png "attiny25-45-servo-library")

[Servo8bit 是一个 AVR 微控制器库，允许你驱动伺服电机](http://www.cunningturtle.com/attiny4585-servo-library/)而不需要 16 位定时器。显然，这对于只有 8 位定时器的较小芯片非常有用，它专门针对 ATtiny45 和 ATtiny85 微控制器。该库提供 256 步分辨率，一次可以驱动多达五个伺服系统。伺服控制脉冲可以在 512 和 2560 微秒之间产生，如果你不介意增加这些脉冲之间的时间[莉雅]说，这将有可能增加 5 伺服限制。

这个库很容易使用，但是在目前的状态下，移植到另一个设备上只需要一点点工作。它是针对 8 Mhz 时钟信号编写的，PortB 用于驱动电机。使用查找并替换来更改 PORTB 关键字以使用 DEFINE 变量应该很容易，但是我们不知道更改时钟频率会有多难。

我们想知道是否有可能使这成为一个从设备，也许实现 1 线协议？