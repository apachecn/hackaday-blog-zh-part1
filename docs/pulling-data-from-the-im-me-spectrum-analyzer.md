# 从 IM-ME 频谱分析仪中提取数据

> 原文：<https://hackaday.com/2010/10/09/pulling-data-from-the-im-me-spectrum-analyzer/>

一个小而便宜的带液晶显示器的频谱分析仪是一个有趣的玩物。但要真正有用，你需要访问原始数据，而且是大量的原始数据。[Travis Goodspeed]着手通过用 GoodFET 和 Python 脚本提取数据来实现这一点。

他从使用 CC1110 芯片的 IM-ME 频谱分析仪开始。他们两人将在 Toorcon 12(名为[真正的男人携带粉红色的寻呼机](http://sandiego.toorcon.org/index.php?option=com_content&task=section&id=3&Itemid=9#lineup))发表演讲，这将被用作演示设备。在研究了数据表之后，他找到了起始 RAM 地址，并做了一些进一步的工作来破译数据是如何存储在其中的。从那时起，问题就是找出获取数据的时机，并编写存储数据的方法。现在，他正在寻找勇敢的灵魂来帮助他开拓这个新发现的工具。看起来，如果你知道你在做什么，并且有足够的耐心，你可以用它来做一点老式的逆向工程。