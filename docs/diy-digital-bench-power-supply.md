# DIY 数字台式电源

> 原文：<https://hackaday.com/2011/06/06/diy-digital-bench-power-supply/>

[Guido Socher]给自己做了一个很棒的小型台式电源,能够在 2 安培下输出 30 伏电压。

这个项目没有采取在 ATX 电源上安装几个抽头的简单方法，而是围绕一个普通的 24 伏笔记本电脑电源模块构建的。ATmega8 产生一个 PWM 信号，该信号通过一个低通滤波器发送，从而可以非常精确地控制一切。这个 DC 信号然后通过 BD245 功率晶体管发送，使一切达到所需的输出。[Guido Socher]包括一个 USB 端口，用于计算机控制一切，最终项目是我们很乐意在我们的工作台上进行的。

我们已经看到一些[计算机电源](http://hackaday.com/2010/12/09/atx-psu-turned-into-an-adjustable-voltage-bench-supply/)被转换成了一个工作台电源，但是我们对【Guido Socher】的构建日志印象深刻。我们并不经常看到超越操作理论的黑客，最终产品也非常好(而且功能强大)。