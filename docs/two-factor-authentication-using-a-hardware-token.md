# 使用硬件令牌的双因素身份验证

> 原文：<https://hackaday.com/2009/10/20/two-factor-authentication-using-a-hardware-token/>

![RSA-SecurID-hardware-token](img/56de0643df84e837fe0402c3d81b5870.png "RSA-SecurID-hardware-token")

不久前，我们遇到了一个朋友，她在周末登录了她雇主的虚拟私人网络。她突然拿出钥匙，从钥匙链上输入一些信息，引起了我们的注意。原来，她的工作为登录网络使用了额外的一层保护。他们实现了一个用户名、pin 码以及一个名为 [SecurID](http://en.wikipedia.org/wiki/SecurID) 的硬件令牌系统。

硬件包括一个带液晶显示屏的钥匙链。一个代码显示在屏幕上，并经常改变，通常是每 60 秒。该设备正在基于 128 位加密种子生成密钥。当这个数字被提供给具有该种子副本的服务器时，它被用作对其他登录数据的附加验证。

这似乎是来自[黄金眼](http://www.imdb.com/title/tt0113189/)的代码生成设备的技术渗透。这确实让我们思考:由于[的问题，免费电子邮件服务已经有了](http://www.networkworld.com/news/2009/100709-gmail-hotmail-yahoo-scam.html)和[的账户盗窃](http://hackaday.com/2008/10/09/palin-hacking-roundup/)，为什么他们不提供包括安全表链的收费服务呢？有了正确的定价结构，这可能是一个很好的供应商收入流。我们还想知道这是否可以用微控制器实现，并用于我们的家庭网络。像往常一样，在下面留下评论，让我们知道你是否已经用这些原则建立了自己的系统。

**更新:**感谢 Andre 的评论，他告诉我们这种类型的[安全可用于 Apache 服务器](http://directory.apache.org/triplesec/)。该发行版包括一个服务器端认证系统和一个基于 Java 的令牌生成器，它可以在任何支持 Java 的手持设备上运行。