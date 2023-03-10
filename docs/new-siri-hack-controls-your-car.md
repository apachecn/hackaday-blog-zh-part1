# 新的 Siri 黑客控制你的汽车

> 原文：<https://hackaday.com/2011/11/28/new-siri-hack-controls-your-car/>

![siri-viper-smartstart](img/707b5f05b4c295bbdb9ab4f553b1ccad.png "siri-viper-smartstart")

Siri 可以预约，告诉你天气，但是现在她也可以启动你的汽车了！

在[我们向你展示了 Siri 如何被黑客攻击](http://hackaday.com/2011/11/21/siri-proxy-adds-tons-of-functionality-doesnt-require-a-jailbreak/)来使用定制代理和执行定制命令之后，我们知道不久之后就会有更多的黑客开始涌入。[Brandon Fiquett]认为如果 Siri 可以远程控制他的汽车就太好了，所以他使用[Pete 的]代理软件将这一功能内置到 Siri 中。

黑客依赖于他安装在汽车上的 Viper 远程启动系统，以及加载到他的代理服务器上的一些模块。他的代理服务器调整允许 Siri 解释预设的命令列表，如“车辆启动”和“车辆启动/解除”，将命令转发给 Viper SmartStart 模块。

我们认为后端功能与现有的 SmartStart iOS 应用程序没有什么不同，但它看起来像是[Brandon]在游戏中击败了 Viper，因为 Siri 尚未向第三方开发者提供。

请观看下面的视频，了解 Siri 的运行情况，然后一定要访问他的网站，查看更多视频以及实现这一点的代码。

[https://www.youtube.com/embed/aPCpqXyFA8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aPCpqXyFA8U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)