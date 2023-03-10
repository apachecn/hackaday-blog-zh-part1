# 转盘音序器被硬币划伤

> 原文：<https://hackaday.com/2009/10/15/turntable-sequencer-scratches-with-coins/>

![scratching-with-arduino](img/0c51f9a10eff4142ce9b026e32bcad29.png "scratching-with-arduino")

[tvst]对音序器有一个有趣的看法。他的设计使用转盘上的硬币来循环触发 midi 事件。有四条轨道可用，每条轨道在旋转平台上方都有自己的传感器。传感器由一个红外发射器和接收器组成，设置为分压器。当有东西从红外发射器下方通过并将红外波反射回接收器时，传感器的输出变为数字高电平。四个传感器连接到 Arduino，Arduino 与 ttymidi 结合使用[，tty midi 将 Arduino 数据转换为 midi 事件。](http://www.varal.org/ttymidi/)

我们喜欢为用户提供更有形界面的项目。硬币很适合这种设置。它们反射的红外线足以触发传感器，而且很容易拾取和移动，不会扰乱其余的轨道。如果能扩展到区分硬币(便士和一角硬币，等等),那就太好了。)以便将分辨率从四个不同的事件增加到八个或更多。休息之后请看视频。T3[https://www.youtube.com/embed/IXOQISfoRks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IXOQISfoRks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)