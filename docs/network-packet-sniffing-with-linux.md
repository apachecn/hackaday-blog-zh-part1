# Linux 下的网络数据包嗅探

> 原文：<https://hackaday.com/2011/01/29/network-packet-sniffing-with-linux/>

![](img/706a49a7ba0ae17d283a292a4f11a869.png "linux-network-sniffing")

这是一个学习一点网络安全知识的机会。这篇文章带我们浏览了一些使用 Linux 工具的网络操作和包嗅探的核心概念。[Joey Bernard]讨论了 tcpdump、p0f 和 dsniff 等包的用法。它们能够记录所有通过计算机连接的网络流量，找出安装在网络上的机器，并监听特定机器的流量。这不会给你一个破解现代网络的步骤。它将提供一些关于您的网络正在发生什么的见解，您应该能够使用这些工具来检查您是否已经采取了足够的安全措施。