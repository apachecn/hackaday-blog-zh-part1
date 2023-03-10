# 黑帽 2008:基于网卡的 Rootkit

> 原文：<https://hackaday.com/2008/08/13/black-hat-2008-nic-based-rootkit/>

![](img/fb8482222b36669db6105782dbc04fb6.png)
虽然[黑帽](http://mahalo.com/Black_Hat)和 [Defcon](http://mahalo.com/Defcon) 都已经结束了，但我们还会发布一些我们认为值得关注的话题。来自 [Clear Hat](http://clearhatconsulting.com/index.php) 的【Sherri Sparks】和【Shawn Embleton】展示了 Deeper Door，利用了 NIC 芯片组。Windows 机器使用 [NDIS](http://en.wikipedia.org/wiki/NDIS) ，网络驱动程序接口规范，在操作系统和实际网卡之间进行通信。NDIS 是一个 API，它让程序员以一种通用的方式与网络硬件对话。大多数防火墙和[入侵检测系统](http://en.wikipedia.org/wiki/Intrusion_detection_system)在 NDIS 级别监控数据包。该团队采用了一种新颖的方法，通过在 NDIS 层以下直接挂接网卡来绕过机器安全。

该团队的目标是英特尔 8255x 芯片组，因为它的开放文档和兼容卡的可用性，如英特尔 PRO/100B。他们发现发送数据非常容易:向特定的内存地址写入一个 UDP 包，检查以确保卡是空闲的，然后告诉它发送。接收端稍微有点困难，因为您必须拦截所有入站流量，并从合法数据包中过滤出您想要的回复。尽管他们编写的是低级芯片组专用代码，但他们说这比编写 NDIS 驱动程序要容易实现得多。虽然这无疑是实现隐蔽通道的一个聪明的方法，但它只能绕过同一台主机上的 IDS 或防火墙，而不能绕过网络上的 IDS 或防火墙。

[图片:[大肥鼠](http://flickr.com/photos/bigfatrat/110453280/)