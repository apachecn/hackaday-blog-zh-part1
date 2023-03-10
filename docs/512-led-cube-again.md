# 512 LED 立方体(再次)

> 原文：<https://hackaday.com/2011/03/18/512-led-cube-again/>

![](img/830fce061c0a63e058a22e7d6e7c32e3.png "LED_cube")

我们以前见过 LED 立方体，但[nick]加大了赌注，他的 8x8x8 LED 立方体在他的微控制器上只使用了三个引脚。

[之前的 LED 立方体](http://hackaday.com/2011/01/02/512-led-cube/)我们已经介绍过使用移位寄存器和锁存器驱动 LED，但是[nick]使用 STP16CP LED 吸收驱动器来减少元件数量。STP16CP 每个可以控制 16 个 led，可以相互级联，工作频率最高可达 30Mhz。使用这样的元件，你会受到微控制器的限制，而不是你的耐心或焊接技能。

当他在邮件中等待他的发光二极管到达时，[nick]决定一头扎进 MATLAB，在动画代码上领先一步。有了立方体上什么好看的想法后，[nick]在他的 PC 上编写了代码，向控制接收器驱动程序的 arduino 发送命令。为了完成这个项目，[尼克]把立方体放在一个非常吸引人的塞满电子设备的木箱上。所有收费，一个非常有效和优雅的建设。

[https://www.youtube.com/embed/U0R9AdIxCq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/U0R9AdIxCq0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)