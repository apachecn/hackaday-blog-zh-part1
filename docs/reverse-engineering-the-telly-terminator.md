# 电视终结者的逆向工程

> 原文：<https://hackaday.com/2010/01/06/reverse-engineering-the-telly-terminator/>

![](img/48d963ebad3471ec699803c2e0281a05.png "telly-terminator")

[奥利弗]收到了电视终结者作为礼物，并决定仔细看看它。这个钥匙扣有两个按钮:一个像手电筒一样点亮 LED，另一个关闭电视。听起来熟悉吗？是的，这也让奥利弗想到了已经消失的[电视](http://hackaday.com/2009/08/17/adafruit-releases-new-tv-b-gone-kit/)。

他打开箱子，只找到几个部件。红外信号背后的大脑是 Helios H5A02HP。只有几个引脚用于输出，因此他连接了一个逻辑分析仪并记录了信号。他的文章很好地涵盖了这一过程。他采用一个已知的红外发射器协议，并将其与逻辑分析仪捕获的数据进行比较。原来，遥控器产生 46 种不同的信号，通过进一步分析得出结论，这里使用的代码有可能来自旧版本的 TV-B-Gone 源。