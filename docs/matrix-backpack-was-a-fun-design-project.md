# 矩阵背包是一个有趣的设计项目

> 原文：<https://hackaday.com/2012/01/23/matrix-backpack-was-a-fun-design-project/>

![](img/ff91ced1da59a3444cbff2c1b6fc4c2d.png "led-matrix-backpack")

[Greg]正在用他的 LED 矩阵背包 PCB 小规模地工作。这是他作为一项活动而设计的玩具。他将自己限制在一块与 8×8 双色 LED 矩阵封装外形完全匹配的电路板上。

您在这里看到的是 PCB 面向 LED 点阵模块底面的一面。让我们称之为董事会的顶部。底部有一个 CR2032 电池座，可以提供足够的电量来运行显示器。由于矩阵是双色的，因此需要驱动大量引脚。[Greg]高端使用三个移位寄存器，低端使用 16 个 N 沟道 MOSFETS。他选择了 MSP430G2201 微控制器，它有一个很好的睡眠模式来节省电能。它没有问题驱动三色动画，因为看到剪辑后休息，但也有一个无人居住的时钟晶体足迹，如果你想把它作为一个时钟。

尽管占地面积小，电路板狭窄，但[Greg]仍然手工焊接所有元件。他甚至在顶部链接的页面上发布了这个过程的延时。

[https://www.youtube.com/embed/sXVhfoKJW7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sXVhfoKJW7E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)