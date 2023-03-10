# 使用 Wii Motion Plus 的四轴飞行器稳定系统

> 原文：<https://hackaday.com/2011/09/14/quadcopter-stabilization-system-using-wii-motion-plus/>

![](img/8deea682bcfbc4bc61dcd8d9aae8c836.png "auto-stabilization-hardware")

如果你正在考虑建造四轴飞行器，这里有一种方法可以在不花大钱的情况下增加稳定硬件。 [BaronPilot 项目使用 Arduino 和 Wii Motion Plus](http://www.elenafrancesco.org/old/arduino/baronpilot) 模块来确保你的飞行项目平稳进行。Motion Plus 内部的硬件包括两个陀螺仪，BaronPilot 可以监控你的飞行装备方向的变化。该项目通过区分遥控器引起的移动和由于风或其他外部因素引起的变化(如在休息后的视频中看到的用棍子击打四轴飞行器)来充当副驾驶。这一切都应该转化为更少的机会，由于操作失误崩溃。

你可以花不到 20 美元买一个 Motion Plus，与我们通常在四轴飞行器中看到的 IMU 板相比，这是一笔不错的交易。这是一个 I2C 设备，使得[很容易连接到任何东西](http://hackaday.com/2010/02/01/wii-motion-plus-direct-pc-interface/)。该项目使用 ATmega328 芯片对 Teensy、Arduino Nano 和 Arduino 克隆提供本机支持。但是 Arduino 平台的可移植性使得调整代码用于任何微处理器变得容易。

[https://www.youtube.com/embed/V9vyUCx3qwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/V9vyUCx3qwY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢费拉拉]