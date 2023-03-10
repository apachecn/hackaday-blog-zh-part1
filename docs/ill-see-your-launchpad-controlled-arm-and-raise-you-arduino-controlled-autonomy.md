# 我会看到你的 Launchpad 控制的手臂，并提高你 Arduino 控制的自主权

> 原文：<https://hackaday.com/2011/11/21/ill-see-your-launchpad-controlled-arm-and-raise-you-arduino-controlled-autonomy/>

![](img/c89be4d3ceb059752dc0b5b582088da9.png "arduino-owi-robot-arm")

这个 OWI 机器人手臂已经被黑进了位置传感器和 Arduino 控制器。[Chris Anderson]看了一眼今天早些时候控制 OWI 的[发射台，说道“等一下，我已经发布了我自己版本的那个项目”。嗯，这会让他知道不要](http://hackaday.com/2011/11/21/ti-launchpad-adds-computer-control-to-a-robot-arm/)[向我们透露](http://hackaday.com/contact-hack-a-day/)他的黑客技术！

位置控制是一个非常好的附加功能。添加到每个关节(肩、肘和腕)的电位计可以通过 Arduino 上的 ADC 引脚读取。只需一点校准就能让微控制器板知道机械臂在任何给定时间的位置。控制技术与 Launchpad hack 相同，但有一个明显的缺点。[克里斯]正在使用阿达果马达驱动盾。它使用 L293D H 桥芯片，但它只有四个通道。这个手臂上有五个马达，所以休息后的视频显示它在没有任何外部指令的情况下四处移动，但你不会看到它抓住任何东西，因为 Arduino 不能移动手爪！

尽管如此，位置反馈使得这个版本的情况。如果你想完全控制，记得订购额外的芯片。

[https://www.youtube.com/embed/agbrwfRiRNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/agbrwfRiRNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)