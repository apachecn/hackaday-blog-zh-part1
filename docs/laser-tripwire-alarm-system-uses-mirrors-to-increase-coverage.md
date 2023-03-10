# 激光绊网报警系统使用镜子来增加覆盖范围

> 原文：<https://hackaday.com/2011/04/18/laser-tripwire-alarm-system-uses-mirrors-to-increase-coverage/>

![laser_tripwire_alarm](img/828fc1adecd9cb9c76f4aa76ce50fe3b.png "laser_tripwire_alarm")

Instructables 用户[EngineeringShock]一直在努力建造一个[激光绊线安全系统](http://www.instructables.com/id/Laser-Trip-Wire-Security-System-with-Combination-L)，配有密码锁。安全系统的工作原理就像你在电影中看到的一样，使用一组镜子将激光反射穿过一个开口几次，以确保空间的安全。

PIC18F1220 微控制器位于报警器的中心，处理其大部分功能。它接收来自激光探测电路的输入，触发蜂鸣器，以及启动和解除整个报警系统。LS7222 数字锁处理密码验证方面的事情，从 16 按钮矩阵键盘接收输入，并告诉 PIC 何时输入了正确的代码。

正如你在下面的视频中看到的，警报系统工作，蜂鸣器相当响。然而，有一个小问题——只有在输入正确的密码并关闭灯后，报警器才会自动启动。他使用的光传感电路过于敏感，只能在黑暗中工作，尽管他讨论了添加更精确的传感解决方案的能力。

如果你有兴趣阅读更多关于激光绊网安全系统的信息，可以看看这个类似的[基于密码的系统](http://hackaday.com/2011/03/11/passcode-protected-laser-tripwire-alarm-system/)，这个内置在玩具中的报警系统，还有这个[基于 Arduino 的报警系统](http://hackaday.com/2010/01/03/arduino-security-with-frickin-laser/)。

[https://www.youtube.com/embed/FenGMQQwgTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FenGMQQwgTg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)