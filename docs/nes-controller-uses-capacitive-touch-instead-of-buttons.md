# NES 控制器使用电容触摸代替按钮

> 原文：<https://hackaday.com/2012/01/19/nes-controller-uses-capacitive-touch-instead-of-buttons/>

![](img/bc3594045c6845b03d6d41495e7b0d4e.png "nes-capacitive-touch-controller")

有一种方法可以真正减少元件数量。[大卫]开发了一个不使用任何按钮的 NES 控制器。铜包层经过打磨，以提供一个基于电容记录按钮按压的焊盘。该板顶部有一个 SIL 接头，便于插入 Arduino 板以读取输入。

[David]无法让 Arduino pin 读取功能足够快地响应 NES 控制台的期望。他最终使用命令直接访问 ATmega 的外围设备，以实现目标计时。说到这里，他使用逻辑分析仪对通信方案进行了自己的嗅探。这项工作的结果，以及董事会文件和代码可在网站上链接以上。在休息之后的剪辑中有一个用于玩超级马里奥兄弟的控制器的演示。

这实际上是一个附带的项目，使用了他通过 Kickstarter 开发的 PCB 工厂。这当然表明，米尔斯工程的设计。T3[https://www.youtube.com/embed/q77DB5VSVzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/q77DB5VSVzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)