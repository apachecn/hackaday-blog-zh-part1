# FPGA 贪吃蛇游戏根本不用 VHDL

> 原文：<https://hackaday.com/2012/01/20/fpga-snake-game-uses-no-vhdl-at-all/>

![](img/adda5d429256afa014d8d44717836196.png "fpga-snake-uses-no-vhdl")

我们真的不应该开始这样的功能；但是这个 hack 是 ***牛逼*** 。这是一个由 FPGA 开发板实现的[贪吃蛇游戏。它采用 16×16 的 LED 矩阵作为显示器，SNES 控制器作为输入。到目前为止，这听起来像是一个非常正常的游戏版本。但是当你在休息后开始听到它是如何工作的，你就会爱上这里正在发生的事情。](http://www.youtube.com/watch?v=niQmNYPiPw0)

首先，它不是用 VHDL——FPGA 的主流编程语言——编写的。相反，[Darrell]使用了纯图解的方法来构建逻辑。好吧，越来越有意思了。随着他继续解释电路，我们开始了解控制输入是如何工作的(非常简单，因为[SNES 控制器使用并行到串行移位寄存器](http://hackaday.com/2011/09/08/arcade-controller-in-a-box/))以及显示是如何多路复用的。但是实际的游戏逻辑才是事情真正开始的地方。显示器中的每个像素都有自己独立的逻辑电路。基本上，每个细胞都有自己的处理器，对传入的信息和随机种子做出反应。这种种子系统被称为“桶旅”，它将一个从一个细胞产卵到下一个细胞的机会传递出去。所有这些加在一起，就构成了一个简单的游戏，而且执行起来非常流畅。T3[https://www.youtube.com/embed/niQmNYPiPw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/niQmNYPiPw0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)