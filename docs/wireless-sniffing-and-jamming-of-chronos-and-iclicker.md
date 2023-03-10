# Chronos 和 Iclicker 的无线嗅探和干扰

> 原文：<https://hackaday.com/2011/01/25/wireless-sniffing-and-jamming-of-chronos-and-iclicker/>

![](img/bf93fc0dbbd2d54a2ab7825222adab93.png "Picture 1")

无线设备无处不在，再加上强大的 RF 开发平台易于访问，使得我们周围的日常世界成为无线黑客的乐园。昨天[Travis Goodspeed] [发布了一篇文章](http://travisgoodspeed.blogspot.com/2011/01/generic-cc1110-sniffing-shellcode-and.html)，展示了 goodfet.cc 如何被用来嗅探无线流量，以及干扰给定的频率。我们之前报道过[的【Travis】从 IM-ME 频谱分析仪](http://hackaday.com/2010/10/09/pulling-data-from-the-im-me-spectrum-analyzer/)中提取原始数据的工作，该分析仪也使用 goodfet.cc

德州仪器的 Chronos 手表开发平台包含一个 C1110 芯片，它可以向感兴趣的嗅探器提供手表的加速度计数据。 [i >点击器](http://www.iclicker.com/dnn/)教室响应设备(内置 XE1203F 芯片)也对此大开方便之门，产生关于你同学投票行为的有趣信息。仍然有一些工作要做，以改善 goodfet.cc 和[特拉维斯]支付啤酒——*不是*提前，请注意。

Chronos 等产品代表着个人区域无线网络的发展趋势，这种安全漏洞最终可能会影响到个人隐私，例如生物数据——尽管如何利用是另一个话题。与这个想法相关的是可嗅探的 RFID 卡数据。越来越多地采用短程无线技术对我们有什么影响，有好有坏？我们邀请你在评论中分享你的想法。