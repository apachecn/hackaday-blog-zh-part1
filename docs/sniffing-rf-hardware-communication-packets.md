# 嗅探 RF 硬件通信包

> 原文：<https://hackaday.com/2011/02/07/sniffing-rf-hardware-communication-packets/>

![](img/6dfac3e631c54636d8ac4be1ed39cedc.png "sniffing-radio-communications")

[Travis Goodspeed]组装了一个概念验证黑客，可以嗅探无线键盘数据包。他正在使用他设计的[下一个希望徽章](http://hackaday.com/2010/06/22/next-hope-badge-hacking-primer/)作为这些测试的硬件平台。它有一个 nRF24L01+板载无线电，可以轻松地与 2.4 GHz 设备通信。

真正的技巧是让无线电监听所有流量，然后将流量缩小到您想要数据的设备。他讲述了所使用的协议，以及他在硬件上绕过 MAC 地址验证的方法。最终，他可以在目标不知情的情况下监听所有键盘数据，并相信只使用徽章上的硬件来注入数据是可能的。