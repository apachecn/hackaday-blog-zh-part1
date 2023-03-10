# 简单皮质，当 Arduino 太弱时用

> 原文：<https://hackaday.com/2012/03/25/simplecortex-for-when-an-arduino-is-too-wimpy/>

![](img/14bca113841099e15fc1d843deb742af.png "board")

有时候，Arduino 就是没有足够的马力。无论您是收集大量传感器数据并通过以太网在网络上发送，还是仅仅尝试构建一个家庭自制视频游戏，都很容易遇到 Arduino 平台的局限性。[Rik]和他的同学们可能会用他们的 [SimpleCortex 开发板](http://www.brc-electronics.nl/)解决这个问题。

SimpleCortex 最初是为了解决 Rik 和他的同学在学校不得不使用的 Arduinos。SimpleCortex 得名于一个运行频率为 120MHz 的 ARM Cortex M3 微控制器；快得足以做一些非常有趣的事情，512kB 的闪存可以容纳更大的程序。

Arduino IDE 不可否认地很糟糕，大型项目对于一个小小的 8 位微处理器来说是一件痛苦的事情。SimpleCortex 通过使用由[库克斯](http://www.coocox.org/)发布的免费[协同中心](http://www.brc-electronics.nl/cocenter-installation) IDE 来改进这个开发环境。CoCenter IDE 支持调试和代码完成，这是任何严肃的桌面编程环境的标准功能。

SimpleCortex 有 Arduino 兼容的头引脚，所以它应该很容易使用现有的屏蔽，如我们本周看到的 [3G 调制解调器](http://hackaday.com/2012/03/21/arduino-shield-includes-everything-but-the-kitchen-sink/)和可以进行[对象跟踪的](http://hackaday.com/2011/06/07/capturing-video-with-an-arduino/) [NTSC 视频 IO 屏蔽](http://hackaday.com/2011/03/24/video-experimenter-shield/)。虽然 SimpleCortex 的规格使其远远落后于 [Raspberry Pi](http://hackaday.com/2012/02/29/raspberry-pi-launched/) ，*有时你不需要 Linux* ，但一个标准的 AVR 或 PIC 是不够的。

目前还不知道这款主板何时上市，但该团队正在与 ITead Studio 合作，正式向外界发布这款主板。