# 沃达丰毫微微蜂窝被黑，根密码泄露

> 原文：<https://hackaday.com/2011/07/14/vodafone-femtocells-hacked-root-password-revealed/>

![vodafone_femtocell_network_diagram](img/b31eebac3ae816eaf597780afd9493f4.png "vodafone_femtocell_network_diagram")

随着电话系统随着时间的推移而发展，破坏它们并利用它们的欲望继续高涨。就在最近，[黑客的选择(THC)]宣布，他们去年通过他们的毫微微蜂窝产品[访问了沃达丰移动电话网络](http://thcorg.blogspot.com/2011/07/vodafone-hacked-root-password-published.html)的安全数据。

毫微微蜂窝的目的是将移动网络覆盖范围扩展到接收可能不理想的地方，通过 IPSec 隧道将呼叫路由到沃达丰的网络。[THC]知道这意味着毫微微蜂窝需要与运营商的传统移动网络进行高级别的交互，所以他们开始四处打探，看看有什么可以利用的。

在使用 root 密码“newsys”获得毫微微蜂窝基站本身的管理权限后，他们发现他们能够允许未经授权的用户使用该服务——这是一个简单的 ToS 违规。然而，他们也有能力迫使任何附近的沃达丰用户的手机使用他们的毫微微蜂窝。这使得他们能够从沃达丰获得密钥，然后在受害者不知情的情况下，利用这些密钥来欺骗受害者的电话和短信。

他们很友好地在他们的 wiki 上发布了所有关于黑客的相关信息，供任何感兴趣的人阅读。现在我们只是想知道美国本土运营商的毫微微蜂窝还要多久才会被以同样的方式利用。

[谢谢，克里斯普]