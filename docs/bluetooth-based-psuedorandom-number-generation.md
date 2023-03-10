# 基于蓝牙的伪随机数生成

> 原文：<https://hackaday.com/2009/12/19/bluetooth-based-psuedorandom-number-generation/>

![](img/dbb6fbd3d27ed72ba302cf1e5ec3abc4.png "bluetooth_prng")

【MS3FGX】做了一个关于使用[蓝牙适配器作为伪随机数产生源](http://www.digifail.com/projects/bt_rng.shtml)()的有趣研究。事实证明， [Bluez](http://www.bluez.org/) 包有一个调用远程蓝牙适配器返回随机数的功能。他从 DealExtreme 上花了大约 30 美元买了 10 个兼容的适配器，并着手组装一些数字，看看它与基于操作系统的 PRNG 相比如何。

因为精确的比较需要数百万个样本，所以时间成了一个问题。适配器对请求的响应有点慢，在第一个 30 秒的测试中只发送了 4800 个数字。这可以通过多台计算机一次访问多个适配器数小时来解决。这能用来做什么？你的猜测和我们的一样好，但是[MS3FGX]在编写他的测试方面做得很好。如果你想生成自己的统计分析，他还提供了一组 2070 万个随机生成的值。