# 以太网控制车库门

> 原文：<https://hackaday.com/2011/12/05/ethernet-controlled-garage-door/>

![](img/9108b7c8a62bcc762c0612bf2fa373b9.png "ethernet")

[托马斯]“车库门开启器是一个很大的老工业单位，所以他没有遥控车库门开启器的便利。显然，过一会儿这就会变得很烦人，所以[Thomas]决定建造一个支持以太网的中继板，这样他就可以用他的 iPhone 开门了。

该系统是基于 ATMega328 和 Microchip 公司的一个小巧的以太网控制器。板上有两个继电器连接到开门器上的向上和向下按钮。该板接收带有“中继 2 开启”等指令的 UDP 包，门相应地做出响应。

仅仅制造一块电路板就花费了[托马斯]区区 43 美元。考虑到新的 Arduino 以太网板的价格约为 60 美元，我们认为他在这里做得很好。从休息后的视频中，我们看到[托马斯]必须按住他的 iPhone 上的按钮才能让门上升。我们看到他的 AVR 上多了几个引脚，因此他的板的 v.2 可能包含一些连接传感器的接头。不过，这是一个非常好的建筑。

[https://www.youtube.com/embed/Eu6lHguMRXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Eu6lHguMRXE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)