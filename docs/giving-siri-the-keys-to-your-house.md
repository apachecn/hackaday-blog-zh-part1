# 给 Siri 你家的钥匙

> 原文：<https://hackaday.com/2011/10/24/giving-siri-the-keys-to-your-house/>

![](img/282517309d0aecf2b2032d4e800c4218.png "siri-actuated-door-lock")

我们还没有真正涉及许多与苹果最新 iPhone 功能 Siri 有关的黑客攻击。我们敢打赌，你已经听说过一堆关于声控人工智能助手，现在你有机会给它你家的钥匙。这个项目[使用 Siri 以一种迂回的方式驱动入口门](http://labs.laan.com/wp/2011/10/unlock-your-door-with-siri-sms-or-a-secret-knock/)上的插销。

这实际上只是在其他几个黑客中看到的短信输入系统的 Siri 前端。门的内部(如上图所示)有一个伺服电机安装在杠杆式锁舌旁边，并通过连杆与之相连。一个配备了无线屏蔽的 Arduino 控制着伺服系统，并在等待来自谷歌应用引擎的指令。但是等等，他们还没有完成。该应用程序引擎连接到一个 Twilio 帐户，这使它能够接收短信。长话短说；Siri 正在发送一条打开门的短信……最终。你可以在休息后的演示中看到，从你第一次访问 Siri 到插销解锁，整个过程需要二十多秒。不过，这是一个很好的第一个原型。

那扇门上有相当多昂贵的五金器具，我们希望能把它们改装成额外的功能。[CC Laan]已经增加了另一种进入方法，使用压电元件来监听秘密敲门。但是我们认为还有改进的空间。由于它是联网的，我们希望看到一个传感器来监控门被打开的频率，也许一个 PIR 传感器可以充当运动感应防盗警报系统。

不需要这么复杂的东西？只实现黑客的秘密敲门部分怎么样？

[https://www.youtube.com/embed/C5cWrTXOvNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/C5cWrTXOvNw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)