# 固态硬盘柔性连接器至 SATA

> 原文：<https://hackaday.com/2011/03/08/ssd-flex-connector-to-sata/>

![](img/1433fdead0e1d1d5d82a5b25e19c38e2.png "2011-03-06 21.17.10.preview")

[Scott]试图修理一台笔记本电脑，我们都知道有时会有什么样的结局。有一个备用的 128GB 固态硬盘和一个戴尔 Mini 10 上网本可以塞进去，只有一个问题，硬盘没有 SATA 连接器。有了这个 [FPC 到 SATA 转换器](http://smg.tophi.net/node/178)，这个问题就像专家一样得到了解决。

受我们最近关于加快 ThinkPad 速度的广告的启发，他能够从类似的三星型号中找到有关 FPC 连接器的信息，订购 SATA 连接器、FPC zero force 连接器和匹配的 24 针跳线。从那里开始，设计一个板来连接两个接口，记录其他驱动器如何布置其 SATA 迹线以确保正常工作。

电路板经过蚀刻，连接器经过焊接，每样东西都插上电源并经过测试，一点点胶水被用来固定普通上网本硬盘中的所有东西，从而实现真正快速的启动时间和工厂外观。