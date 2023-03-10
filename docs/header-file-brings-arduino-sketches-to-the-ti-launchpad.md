# 头文件将 Arduino 草图带到 TI 启动板

> 原文：<https://hackaday.com/2011/03/09/header-file-brings-arduino-sketches-to-the-ti-launchpad/>

![](img/59defee26541561027d0e036092f98cc.png "TI-Launchpad-arduino-code")

[Chris Hulbert]正在让 Arduino 用户使用[头文件编写 MSP430 芯片变得更容易，该头文件允许你为 Launchpad](https://github.com/chrishulbert/friendly_launchpad) 编译 Arduino 草图。这是有意义的，因为越来越多的 Arduino 草图可用，TI Launchpad 的低成本是一个很好的伙伴。实现这一点并不难，尽管你还不能找到对所有 Arduino 功能的支持。

在撰写本文时，[Chris]只有 51 行代码致力于这个项目。它为 setup()、loop()、delay()、pinMode()、pinBit()、digitalWrite()和 digitalRead()提供了宏。您会注意到头文件最重要的部分之一是它为用户禁用了看门狗定时器(这是许多 MSP430 初学者的绊脚石)。这是一个有趣的解决方案，但要真正有用，我们希望看到硬件与 Arduino IDE 的集成。除此之外，Arduino 的其他功能也唾手可得。获取编码并将您的推送请求提交给[Chris]以包含在他的存储库中。

[谢谢克里斯]