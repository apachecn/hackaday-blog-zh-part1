# 避免 Windows 中的操作系统指纹

> 原文：<https://hackaday.com/2008/10/04/avoiding-os-fingerprinting-in-windows/>

![](img/dad3330780d1f74a3dcb409b5126b650.png "fingerprint")

[Irongeek]一直致力于改变他的 Windows 盒子的操作系统指纹。常见的网络工具如 [Nmap](http://nmap.org/) 、 [P0f](http://lcamtuf.coredump.cx/p0f.shtml) 、 [Ettercap](http://ettercap.sourceforge.net/) 和 [NetworkMiner](http://networkminer.wiki.sourceforge.net/NetworkMiner) 可以通过 TCP/IP 栈的行为来确定正在运行什么操作系统。通过改变这种行为，您可以使您的系统看起来像另一个操作系统。[Irongeek]通过检查[安全斗篷](http://www.securiteam.com/tools/5MP052KI0A.html)的源代码来找出哪些注册表项需要更改，从而开始编写自己的工具。他的 OSfuscate 工具可以让你定义你自己的。操作系统指纹文件。从 IRIX 到 Dreamcast，你可以伪装成任何数量的不同系统。不幸的是，这只适用于 TCP/IP。其他方法，如 [Satori](http://myweb.cableone.net/xnih/mortalx.htm) 基于 DHCP 的指纹识别，仍然有效，需要通过其他方式绕过。没错，这只是“通过默默无闻获得安全感”，但却是一件好玩的事情。