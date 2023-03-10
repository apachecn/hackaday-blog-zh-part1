# RFID 控制的电话拨号

> 原文：<https://hackaday.com/2009/03/14/rfid-controlled-phone-dialing/>

![phone1](img/dbe1722325678b94cae8b29e3dfd4f26.png "phone1")

为了给老年人创造一个更容易使用的界面，[Stephen]组装了这个使用 RFID 标签拨打的[电话原型。随着年龄的增长，我们的运动技能和视力退化是很常见的。有一些特殊的手机，但一般来说，它们唯一的变化是加大了按钮和扬声器。[Stephen]有一个想法，想做一个系统，让一个老人拿着一张他的照片给电话，电话就会拨号。他拿起一个 RFID 读卡器和一个 Arduino。RFID 阅读器的代码已经有了，为了防止因手抖或动作缓慢而导致的多次刷卡，他做了一些小小的修改，就能让它很快工作起来。Arduino 然后将数据发送到 ioBridge 进行呼叫。他正在使用](http://cygnetengineering.blogspot.com/2009/03/rfid-activated-phone-system.html)[谷歌语音](https://www.google.com/accounts/ServiceLogin?passive=true&service=grandcentral&ltmpl=bluebar&continue=https%3A%2F%2Fwww.google.com%2Fvoice%2Faccount%2Fsignin%2F%3Fprev%3D%252F&gsessionid=WFeppimwNfo)来实际拨打电话，所以你也可以将它应用到其他服务上。休息之后你可以看到一段视频。

[https://www.youtube.com/embed/B-NNGHiohzE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/B-NNGHiohzE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[Stephen]指出，尽管他在视频中使用的是 iPhone，但这个项目实际上应该适用于任何两部手机。