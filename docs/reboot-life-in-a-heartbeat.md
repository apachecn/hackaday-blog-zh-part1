# 瞬间重启生活

> 原文：<https://hackaday.com/2010/02/18/reboot-life-in-a-heartbeat/>

![](img/25dd32ce000867364395c7e68f0bd05c.png "ekg-life")

这件[连帽衫可以感应你的心跳，并用它来控制生活](http://jmsaavedra.com/weblog/?p=850)。康威的生命游戏在[各种电子项目](http://hackaday.com/2009/09/28/capacitive-buttons-control-all-life/)中很流行，它使用一个细胞网格加上[一套规则](http://en.wikipedia.org/wiki/Conway%27s_Game_of_Life#Rules)来模仿简单生物的生与死。这种迭代在你自己的心脏上显示游戏，然后接入你的心率，在每个心动周期开始时重置游戏。我们猜想你可以说，只有你不这样做，生活才会继续。

检测心跳的 [EKG 电路](http://johnhenryshammer.com/TEChREF/opAmps/IRHEARTSCHMATIC.html)是由一个红外发射器通过你的指尖照射到一个接收器上组成的。运行 Arduino 引导程序的 ATmega168 控制 EKG 电路，并重置负责生命的 ATmega48。[乔]承认这是矫枉过正，但他目前没有一个 AVR 程序员；他走这条路是为了成功。时髦的极客帽衫是一个测试运行(呃…测试跳？)休息之后。

[https://player.vimeo.com/video/9528724](https://player.vimeo.com/video/9528724)