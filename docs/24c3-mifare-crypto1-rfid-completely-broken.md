# 24C3 Mifare Crypto1 RFID 完全损坏

> 原文：<https://hackaday.com/2008/01/01/24c3-mifare-crypto1-rfid-completely-broken/>

我们在 CCC 上的另一个亮点是[Karsten Nohl]和[Henryk pltz]展示了他们如何逆转 Philips crypto-1“经典”Mifare RFID 芯片，这种芯片用于汽车钥匙等。他们分析了硅和实际的射频握手。看着他们发现的关于 10K·盖茨的硅片。用 Matlab 分析发现了 70 个独特的函数。然后，他们开始寻找“类似密码”的部分:用于寄存器、xor 的一长串触发器，靠近边缘的东西，它们是高度互连的。只有 10%的门被加密了。他们现在知道了基于这一分析的加密算法，并将在今年晚些时候发布。

随机数生成器最终只有 16 位。它根据卡通电后的时间生成该数字。他们控制阅读器(一个 [OpenPCD](http://www.openpcd.org/) )，让他们一遍又一遍地生成相同的“随机”种子数。这实际上是在他们发现缺陷之前偶然发生的。

名单上又多了一个漏洞百出的蒙昧安全系统。为了获得更多乐趣，[观看演示视频](http://video.google.com/videoplay?docid=4252367680974396650&hl=en)。

*   [永久链接](http://events.ccc.de/congress/2007/Fahrplan/events/2378.en.html)