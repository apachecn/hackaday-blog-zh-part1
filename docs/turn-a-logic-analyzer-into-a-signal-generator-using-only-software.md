# 仅使用软件将逻辑分析仪变成信号发生器

> 原文：<https://hackaday.com/2011/05/24/turn-a-logic-analyzer-into-a-signal-generator-using-only-software/>

![](img/814667c322153b2050a17ac5f9df2fb3.png "PwmLogic_Async")

我们通过看[阿尔顿·布朗]所有这些美食剧集学到的一件事是，多任务者比单任务者好得多。[Joost]正沿着同样的思路思考，采用一个奇妙的工具，并为其添加一个有用的功能。他的软件项目[将 USB Saleae 逻辑分析仪变成信号发生器](http://brrrbaybay.com/index.php/pwm-logic-202121545/about)。

已经有很多理由去拥有这些神奇工具中的一个。但使用它来产生多达 8 个通道的 PWM 信号的能力是一个受欢迎的补充。它能够以 4 MHz 的采样速率产生 1Hz 至 1MHz 的频率。它使用原始的 SDK，不需要对硬件做任何改变(我们会认为新的固件是必要的，但幸运的是事实并非如此)。有一点需要注意的是，目前这只适用于运行。NET 3.5 版或更高版本。看起来 MSI 安装包是所有可供下载的东西，所以很容易将其移植到其他操作系统的想法已经破灭，除非[Joost]决定分享他的源代码。

编辑 2016 年 7 月 12 日:[Joost]的网页宕机了，[但是他把它移到了 Github](https://github.com/joosthaverkort/PWMLogic) 。