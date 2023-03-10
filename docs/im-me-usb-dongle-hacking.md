# 即时消息 USB 加密狗黑客

> 原文：<https://hackaday.com/2010/10/23/im-me-usb-dongle-hacking/>

![](img/25ea6bfc046aa0eceff80ecfe9417334.png "IM-ME-dongle-hacking")

这个电路板来自一个女孩技术 IM-ME 的 USB 加密狗。[Joby Taffey]把它拆开，[四处探查，了解它的秘密](http://blog.hodgepig.org/2010/10/22/im-me-usb-dongle-hacking/)。这些加密狗和粉色寻呼机一起出现，已经成为 T2 流行的低成本黑客平台 T3。但到目前为止，我们还没有看到对加密狗本身做了多少工作。

[Joby]使用了[OpenBench 逻辑嗅探器](http://hackaday.com/2010/02/28/open-source-logic-analyzer-2/)来了解这里发生了什么。该板上有两个芯片，一个是 Cypress CY7C63803 USB 微控制器，它通过 USB 与计算机通信，还通过 SPI 与 Chipcon CC1110 SoC 无线电通信。看来重新编程 Cypress 芯片是行不通的，所以他去研究 CC1110。他通过嗅探 SPI 线路获得的芯片间通信数据为他提供了使用自己的固件重新实现协议所需的一切。作为概念验证，他重新闪存了 CC1110，现在可以发送和接收来自加密狗的任意命令。广告之后有一个小视频，显示电脑上的一个脚本打开和关闭加密狗的 LED。

[https://www.youtube.com/embed/IN29hRLuAic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IN29hRLuAic?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)