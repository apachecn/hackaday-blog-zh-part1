# 使用电容耦合的以太网连接

> 原文：<https://hackaday.com/2010/10/26/ethernet-connection-using-capacitive-coupling/>

![](img/23d477261c9e319367047c9366efeef2.png "ethernet-via-capacitive-coupling")

想要在他的项目构建中节省空间和重量[Florin]开始寻找一种方法来在没有磁性的情况下添加以太网连接。他不明智的第一次尝试包括直接耦合两个开关，在这个过程中同时烧坏两个开关。经过一些研究，他发现以太网硬件制造商已经考虑到需要没有磁性的设备，并且有几篇关于这个主题的应用笔记。[Florin]根据 Realtek 提供的器件信息，了解到它们可以容性耦合。在减少了第二对开关的磁性元件后，他在试验板上连接了一些电阻电容网络，并使连接工作起来。