# Slowloris HTTP 拒绝服务

> 原文：<https://hackaday.com/2009/06/17/slowloris-http-denial-of-service/>

![](img/22718d2fadac6cf95281f9f71d3e07a8.png)

[RSnake]已经开发了一种拒绝服务技术,可以更有效地关闭服务器。传统上，[执行拒绝服务攻击](http://ha.ckers.org/blog/20090504/using-denial-of-service-for-hacking/)需要向服务器发送数千个请求，这些请求不必要地占用资源，直到服务器出现故障。这种重复的攻击要求请求快速连续地发生，并且通常是分布式的。然而，[RSnake]新技术让客户机打开几个 HTTP 会话，并尽可能长时间地保持它们打开。大多数服务器被配置为只处理一定数量的连接；无限会话会阻止合法请求得到处理，从而关闭站点。此漏洞存在于使用线程的 web 服务器上，如 Apache。

黑客攻击的一个积极的副作用是服务器不会崩溃，只有 HTTP 服务器会受到影响。他的示例 perl 实现 [slowloris](http://ha.ckers.org/slowloris/) 能够只用一台计算机就瘫痪一个普通的网站。一旦攻击停止，网站将立即恢复在线。

**更新:读者【Motoma】发来一个 [python 实现](http://motomastyle.com/pyloris-a-python-implementation-of-slowloris/)的 slowloris 调用[幽门](http://pyloris.sourceforge.net/)**

[图片:[萌破](http://www.youtube.com/watch?v=rLdQ3UhLoD4)