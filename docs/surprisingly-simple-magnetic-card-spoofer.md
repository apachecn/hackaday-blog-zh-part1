# 出奇简单的磁卡欺骗器

> 原文：<https://hackaday.com/2010/11/27/surprisingly-simple-magnetic-card-spoofer/>

![](img/87295fed6f7af5633354ee37b3cf1a79.png "magnetic-card-spoofer")

【克雷格的】[磁卡欺骗器](http://flashingleds.wordpress.com/2010/11/12/magnetic-swipe-card-spoofers/)既简单又高明。欺骗这些卡片有两个部分，他都处理好了。第一部分是获取实际的卡数据。为此，他设计了一个带有接头的欺骗板，该接头连接到一个读卡器。第二部分是恶搞本身，用电磁铁完成。就像[过去的欺骗者](http://hackaday.com/2010/11/02/magnetic-card-stripe-spoofer/)一样，他用涂有珐琅的电磁线包裹了一个垫片。一把旧刀片被选中是因为它的厚度和[铁磁性](http://en.wikipedia.org/wiki/Ferromagnetism)。该磁铁由存储数据的 ATtiny2313 驱动，并由驱动线圈的晶体管保护。他的电路板有一些设计缺陷，但[Craig]能够从欺骗中获得与原始卡相同的跟踪数据，尽管 LED 被用作保护二极管和晶体管基座上的“售后”电阻器。