# Scam-o-Matic 确定您是否购买了假 SD 卡

> 原文：<https://hackaday.com/2011/12/07/scam-o-matic-determines-if-you-bought-fake-sd-cards/>

![](img/94ba795e7902f3a3e35a3231b0e016c1.png "necromant")

[【Andrew】最近在购买 SD 卡时被骗](http://necromant.ath.cx/wp/2011/12/06/scam-o-matic/)他发明了一个小工具，可以帮助你判断自己是否被骗了。

你看，他买了一套 MicroSD 卡，宣传的容量都是 4gb。当他试图使用它们时，它们都无法写入超过 115 兆字节的数据，所以他知道有事发生了。他坐下来用一些工具，可以用来检查闪存介质的实际容量，但他说，他们难以置信地慢扫描卡。

当他等待其中一次扫描完成时，他决定创建一个自己的实用程序，可以在很短的时间内完成同样的事情。他的快速而肮脏的应用程序名为“Scam-o-Matic”，向卡中写入随机数据，双重检查写入的区域，以确保数据可以被读回。如果它发现错误，您的卡可能是假的或损坏的，但如果不是，它会自动准备媒体使用。

显然这种情况比较少见，但是如果你认为你捡到了一些可疑的 SD 卡，一定要去查看一下[Andrew 的] [Github 仓库。](https://github.com/nekromant/scam-o-matic)