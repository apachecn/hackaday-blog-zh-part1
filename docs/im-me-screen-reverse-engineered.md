# 即时消息屏幕反向工程

> 原文：<https://hackaday.com/2010/02/01/im-me-screen-reverse-engineered/>

![](img/23e4e22075ab234c9554ad63b15f6d5a.png "IM-ME-screen-reverse-engineered")

[Dave] [找出了 IM-ME 终端](http://daveshacks.blogspot.com/2010/01/im-me-lcd-interface-hacked.html)的命令集。让这个[粉色塑料外设](http://hackaday.com/2009/11/30/pink-wireless-terminal-of-wonder/)放弃这些秘密需要一点侦查。他用示波器嗅出 SPI 连接，然后用[一个被黑客攻击的 IM](http://hackaday.com/2010/01/06/update-more-pink-wireless-terminal-hacking/)捕捉来自一个新出厂单元的流量。他设法推断出写数据是如何被发送的，但是他仍然不能弄清楚命令是如何从那些数据中区分出来的。有了手头的信息，他在互联网上搜索，发现屏幕使用的是 ST7565S 控制器。现在，他有了定制的固件来让 LCD 显示屏执行他的命令，我们想知道接下来会发生什么？