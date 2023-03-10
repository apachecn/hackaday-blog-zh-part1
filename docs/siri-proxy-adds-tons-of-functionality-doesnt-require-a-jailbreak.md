# Siri 代理增加了大量功能，不需要越狱

> 原文：<https://hackaday.com/2011/11/21/siri-proxy-adds-tons-of-functionality-doesnt-require-a-jailbreak/>

![siri-proxy](img/8c9e13a7d9384cb440cf2bcbd099c0b3.png "siri-proxy")

[Pete]有一部 iPhone 4s，喜欢 Siri，但他希望她有更多的内置功能。虽然该应用在技术上仍处于测试阶段，可能会在不久的将来进行更新，【Pete】现在想要更多的功能。

由于苹果并不以开放的架构著称，他不得不变得有创意。由于 Applidium 公司的人知道 Siri 的命令是如何传递给苹果的，他组装了一个代理服务器，允许他拦截和处理数据。

黑客相当狡猾，甚至不需要越狱。一点 DNS 和 SSL 欺骗被用来引导 Siri 的 WiFi 流量通过他的服务器，然后服务器将命令转发给苹果的服务器进行处理。在回程中，他的服务器解释数据，寻找他定义的自定义命令。

在下面的视频中，他简要介绍了该系统，然后花了一些时间展示他如何使用 Siri 来控制他的 WiFi 恒温器。虽然这个过程只有在 Siri 通过 WiFi 连接到他的家庭网络时才有效，但它仍然非常棒。

[https://www.youtube.com/embed/AN6wy0keQqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AN6wy0keQqo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)