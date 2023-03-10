# ARP 中毒仍然是一个问题

> 原文：<https://hackaday.com/2008/06/04/arp-poisoning-is-still-a-problem/>

毫无疑问，你已经听说了托管漏洞框架 Metasploit 的网站在本周早些时候被[黑了](http://seclists.org/fulldisclosure/2008/Jun/0011.html)，但是你可能没听说过的是[使用第二层攻击](http://taosecurity.blogspot.com/2008/06/old-school-layer-2-hacking.html?showComment=1212545100000#c7102389871482079713)。虽然 Metasploit.com 并没有被真正破解，但是同一个 VLAN 上的一台服务器被入侵并被用来对网关进行 ARP 攻击。 [ARP 中毒](http://en.wikipedia.org/wiki/ARP_poisoning)是一种通过向以太网路由器发送虚假 ARP 报文，将黑客的 MAC 地址与来自真正网络节点的有效 IP 地址关联起来，从而嗅探数据的方法。从那里，黑客能够发动他们的 MITM 攻击，并显示上面的图像，而不是 Metasploit 的网站。如果 ISP 使用固定的 ARP 条目，这个问题本来是可以避免的，而这正是[HD Moore]必须做的事情，以使网站恢复在线。[Richard Bejtlich]指出，尽管最近大多数人都在关注应用程序的安全性，但像这样的基本攻击仍然会发生。如果你在保护自己方面做得很好，当在共享主机环境中运行时，你仍然会受到第三方安全性的支配。

*   [永久链接](http://taosecurity.blogspot.com/2008/06/old-school-layer-2-hacking.html)