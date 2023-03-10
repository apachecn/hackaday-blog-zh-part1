# 自动化协议分析

> 原文：<https://hackaday.com/2009/01/13/automated-protocol-analysis/>

![wireshark](img/0db5a6736b2d5e5ab2268cca10a5e522.png "wireshark")

作为工作的一部分，BreakingPoint 实验室的 ruid 已经做了相当多的协议逆向工程。他整理了一个[帖子，介绍了一些对这项任务有用的工具](http://www.breakingpointsystems.com/community/blog/automated-protocol-reverse-engineering)。基于文本的协议有许多人类可读的字符，可以帮助您识别字段。但是二进制协议没有这种奢侈。他推荐了解决这些情况的[协议信息项目](http://www.4tphi.net/~awalters/PI/PI.html "The Protocol Informatics Project")。它将生物信息学算法应用于网络流量。你给它一个协议的数据包转储，它会比较它们，找到相似之处，就像比较基因序列一样。它可能会被浪费大量空间的协议所混淆，但它仍然是一种非常聪明的逆转方法。

[图片: [slashcrisis](http://flickr.com/photos/bastard_admin/2556829596/ "Trying to fetch AIS packages... on Flickr - Photo Sharing!")