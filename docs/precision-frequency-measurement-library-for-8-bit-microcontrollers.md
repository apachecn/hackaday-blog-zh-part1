# 8 位微控制器的精密频率测量库

> 原文：<https://hackaday.com/2011/06/03/precision-frequency-measurement-library-for-8-bit-microcontrollers/>

![](img/1ea67c28cd518fa74b62cbda52b4d934.png "frequency-measurement-library-for-8bit-microcontrollers")

[Paul]一直致力于移植 Arduino 库以用于 Teensy 微控制器平台。这很简单，因为它们都使用相同的 Atmel 芯片架构。但是偶尔他会发现 Arduino 库并不像他们被吹捧的那样。当希望移植一个频率测量库时，他最终[编写了自己的更好用、更便携的库](http://www.pjrc.com/teensy/td_libs_FreqMeasure.html)。

他对 Arduino 频率计数器库有两大不满。首先，它要求使用精确的频率计数器校准补偿系数。这是一个先有鸡还是先有蛋的问题，因为许多用 Arduino 构建频率计数器的人这样做是因为他们还没有一个独立的工具。第二个问题是 Arduino 库是为 ATmega168 或 ATmega328 芯片硬编码的。

这个新的库通过一个折衷解决了这两个问题。您的硬件设置必须使用晶体振荡器。你可以在上面的图片中看到，用这种方法测量频率非常准确。该封装还使用了一个很薄的抽象层，可以很容易地移植到任何用 c 编程的 8 位微控制器上。