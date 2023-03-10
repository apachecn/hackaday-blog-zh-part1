# 快门触发遥控器有一些很好的设计考虑

> 原文：<https://hackaday.com/2011/11/04/shutter-trigger-remote-with-some-nice-design-considerations/>

![](img/8558e1a88b27db4520225f4af6119bae.png "shutter-trigger-remote")

下面是【卢卡斯的】[红外相机遥控器](http://www.iwasz.pl/soft/canon-ir-remote-2/)的胆量。他以现有的设计为基础，但是寻找可以改进的地方。他觉得在这种情况下，ATtiny2313 有点浪费。但是进一步的调查让他明白了为什么选择它。如果您使用 ATtiny13，连接晶体振荡器的能力就会丧失(该芯片仅提供 1 引脚时钟信号输入)，内部 RC 振荡器也达不到他的可靠红外通信标准。

何频没有使用 AVR 直接驱动红外 LED，而是使用了晶体管，希望在使用时能让最大电流流过二极管。我们不确定它是否有必要，但我们可以看到它是如何有意义的。电源来自一个未经调节的 3 伏硬币电池，因此，随着时间的推移，电压可能会下降，这将发挥作用。

说到硬币电池，电池寿命是一个问题。[Lukasz]正在使用 AVR 的睡眠功能，使用时间为三秒钟。这应该能让细胞存活相当长的时间。但是他用万用表测得的 0 伏电压是异常的。为了获得微小电流的精确测量，您需要额外的设备，如[达夫·琼斯] [uCurrent adapter](http://www.alternatezone.com/electronics/ucurrent/) 。

这个佳能相机兼容项目的示意图只以 Eagle 格式提供，所以为了您的方便，我们在休息后嵌入了它的图像。如果你把我们周四看到的 TV-B 快门释放中的一些代码换出来，用尼康做这个应该没问题。

[![](img/758e52fcce809ef978e43a0a8baa34d6.png "cannon-ir-remote-schematic")](http://hackaday.com/wp-content/uploads/2011/11/cannon-ir-remote-schematic.png)