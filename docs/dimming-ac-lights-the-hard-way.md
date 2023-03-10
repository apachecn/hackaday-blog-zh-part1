# 调光交流电灯困难重重

> 原文：<https://hackaday.com/2011/12/12/dimming-ac-lights-the-hard-way/>

![](img/80dddbac7a257b0fa3641ce36f748859.png "AC")

又到了一年中温度计下降、太阳落山较早的时候，我们试图用冬至节来温暖我们的心，这在我们各自的文化中都很常见。当然，我们都需要几串灯，但如果我们有 [PWM 控制的可调光灯](http://familab.org/blog/2011/12/dimmable-ac-light-box/)不是很好吗？

当他开始研究 PWM 控制、交流供电的灯箱时，[Waterbury]立即意识到继电器不是最佳解决方案。摆脱他陷入的困境的最佳途径是通过[零交叉](http://familab.org/blog/2011/12/dimmable-ac-light-box/5/)。在将一个变压器连接到一个用于检测电路的晶体管上之后，一小段代码在凌晨时分被编写出来，并且有了一个[概念证明](http://www.youtube.com/watch?feature=player_embedded&v=foCL79vxxK4#!)。

控制盒完成后，[Waterbury]编写了一个快速的 [VB 应用程序](http://familab.org/blog/2011/12/dimmable-ac-light-box/8/),并通过串口将 WinAmp 可视化器的输出输入到灯光中。《T2》*《盗梦空间》*演示很棒，但是需要更精细的控制。在看到一个黑客在一个漂亮的[均衡器芯片](http://hackaday.com/2011/10/10/character-lcd-spectrum-analyzer-made-simple-with-a-dedicated-ic/)上的每日帖子后，IC 上的七个波段输出被转换为 UART。

[Waterbury]带着他的七波段交流控制灯箱和他的合成器去了一个万圣节派对，结果看起来棒极了。你可以在休息后看看，但我们真的很期待看到他今年的圣诞装饰。

[https://www.youtube.com/embed/tVzEp0hbRbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tVzEp0hbRbg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)