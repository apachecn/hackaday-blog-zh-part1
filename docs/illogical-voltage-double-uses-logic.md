# 不合逻辑的倍压使用逻辑

> 原文：<https://hackaday.com/2011/10/21/illogical-voltage-double-uses-logic/>

![](img/2b52d5b78ec82fb178f32c5d203db217.png "74hc14_output_gnd_doubler")

刚刚写完 7400 逻辑竞赛的参赛作品。这是一个使用 74HC14 逻辑芯片的倍压器。因为这根本不是芯片的本意——而且他很喜欢双关语——他称之为[不合逻辑的迪克森倍增器](http://jethomson.wordpress.com/2011/10/19/7400-competition-illogical-doubler/)。

他在这里得到的基本上是由一组二极管和电容器组成的电荷泵。在试验板上，您可以看到两个芯片，一个用作时钟信号发生器，另一个用作电荷泵的一部分。我们已经看到了一连串的黑客攻击，他们在逻辑芯片的输入端使用保护二极管。事实上，[乔纳森的]设置使用了与[准系统 PIC RFID 标签](http://hackaday.com/2011/09/26/barebones-pic-rfid-tag/)相同的反向供电概念。你可能还记得在那个项目中，芯片是由一个 I/O 引脚供电的，VCC 引脚没有连接到任何东西。

我们在休息后嵌入了一个视频，展示了一些电压测量结果，以及一个由倍频电路供电的 LED。

[https://www.youtube.com/embed/E8lNV-ntBpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/E8lNV-ntBpU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)