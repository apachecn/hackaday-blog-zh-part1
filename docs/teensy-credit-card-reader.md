# 青少年信用卡读卡器

> 原文：<https://hackaday.com/2010/07/24/teensy-credit-card-reader/>

![](img/3d60ee63266920b61b2d81e8b765ebbb.png "teensy-mag-reader")

这里有一个商业上有意义的方法。[PT]回忆起去年的 HOPE 会议，当时他们的展位使用虚拟信用卡终端进行购物，需要手动输入信用卡信息。今年他们将拥有相同的虚拟终端，但这个磁条阅读器会自动填写。

Mouser 的磁条阅读器(只读，[这里没有有趣的事情](http://hackaday.com/2009/09/23/universal-cc/))从卡上抓取数据。一个 Teensy 微控制器板，它将自己标识为 USB 键盘，从解析的数据中自动填充虚拟终端。真正的问题是，他的客户愿意让他们的信用卡通过被黑的读卡器吗？