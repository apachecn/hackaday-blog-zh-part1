# Nexus One 的外部文本显示

> 原文：<https://hackaday.com/2011/07/01/external-text-display-for-nexus-one/>

![Nexus One External Display](img/ea931d971da2d36a605362f982d79aa1.png "nexusonelcd")

[follower]为他的 Nexus One 制作了一个 2 线外部显示器的原型，使用了一个带 USB 主机屏蔽的 Arduino 和 Android 开放附件协议。有两个基本的软件在工作:一个 Arduino sketch 处理显示手机发送的数据，一个轻量级的 android 应用程序检测外部屏幕的存在并向其发送数据。如此处所示，它显示最近收到的短信的时间和开始时间。

这个项目结合了[follower]一直在做的其他几件事情，包括 USB 附件、后台服务、与 Arduino 的接口和处理 SMS 消息，所以它是模块化和开源的。如果你对混合微控制器项目和你的 android 手机感兴趣，这个项目中有很多东西可以帮助你起步。

就黑客而言，这很大程度上是一种“因为你可以”的交易，旨在将一堆很酷的东西绑在一起。你不太可能很快看到我们在口袋里带着液晶显示器和试验板，但它为一些潜在的有趣的手机配件铺平了道路。