# 挑战:弄清楚这个基于逻辑的追踪器是如何工作的

> 原文：<https://hackaday.com/2012/01/25/challenge-figure-out-how-this-logic-based-chaser-works/>

![](img/a23f5302bac43b5c5b0b70c98b9dd5cd.png "logic-based-chaser")

[Andrea] [用一个逻辑芯片制造了这个 LED 追踪器](http://www.instructables.com/id/LED-chaser/)。它点亮六个 led 中除一个之外的所有 led，dim 位以追逐顺序沿该行来回移动。这有点像一个没有衰落尾巴的逆[拉森扫描仪](http://hackaday.com/2011/10/28/detailed-tutorial-shows-how-to-unleash-your-inner-michael-knight/)。但是用逻辑芯片而不是微控制器来做这件事是一个有趣的挑战。

这就引出了这个特性。[安德里亚]没有真正张贴电路如何工作的解释。通常遗漏的细节意味着我们将提示存档，然后继续下一个，但是我们认为这提供了一个有趣的活动。你能弄清楚电路是如何工作的吗？我们已经知道它使用的是 CD4017 十进制计数器/分频器芯片。它从 555 定时器电路获得时钟信号。[Andrea]的原理图有点难读，但如果需要，可以拿一份副本，放大一点(或使用浏览器缩放功能)并研究 [CD4017 数据手册](http://www.datasheetcatalog.org/datasheets/90/108738_DS.pdf) (PDF)。

想要证明它确实有效吗？休息后嵌入。

[https://www.youtube.com/embed/WXmFH5tPrCA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WXmFH5tPrCA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)