# 工具:Saleae 逻辑、逻辑分析仪

> 原文：<https://hackaday.com/2009/03/06/tools-saleae-logic-logic-analyzer/>

逻辑分析仪记录两个芯片之间的总线通信。如果你曾经遇到过让两个芯片说话的问题，或者想对一个协议进行逆向工程，那么逻辑分析仪就是你需要用来窥探总线的工具。

[逻辑](http://www.saleae.com/logic/)是一个 USB 逻辑分析仪，有八个通道，采样率高达 24MHz。在业余爱好水平的逻辑分析仪中，逻辑具有良好的混合功能和体面的采样率。我们已经关注乔·加里森在逻辑方面的工作很长时间了。如果你曾经考虑过将产品推向市场，你可以从[乔的博客](http://saleae.vox.com/)中学到很多，他的博客记录了他的开发过程。

刚出道的时候，这个逻辑太受欢迎了，以至于很难买到一个。它现在已经被广泛使用，Saleae 给了我们一个来尝试。阅读下面我们的评论。

*逻辑分析仪与示波器*

大多数现代电子项目从逻辑分析仪中获益比从示波器中获益更多。示波器显示模拟电压随时间变化的图形，如正弦波曲线。逻辑分析仪只检测高和低数字状态，但它同时记录许多信号。逻辑分析仪将数据转储到计算机进行分析，很少有示波器具有这一功能。

*你得到了什么*

*![whatugetiv](img/4ee47c30214d967bbefd369cd6f3e565.png "whatugetiv")
*

逻辑封装在外部硬盘盒中。分析仪是一个小的阳极氧化铝圆盘，带有激光蚀刻的信号标记。它比我们预期的要小得多，比紧凑型闪存卡略小。包括一根 mini-B USB 电缆。

一根粗规格电缆和九个 [E-Z 钩](http://www.e-z-hook.com/Html/MicroHooks.html)(图中显示了 5 个)将逻辑电路连接起来。挂钩的触感真的很好；按下挂钩的背面以露出一对镊子，抓住信号线，然后缩回以将其固定到位。可伸缩镊子防止狭窄测试电路上的意外短路。

软件不包括在内，取而代之的是，你可以从 Saleae 网站得到指令[下载](http://www.saleae.com/downloads/)最新版本。我们总是下载最新的软件，所以我们很高兴少了一张被扔进垃圾填埋场的 CD。

目前，只有 Windows XP/Vista 软件可用，但 Mac 和 Linux 软件[应该很快就会准备好](http://saleae.vox.com/library/post/inventory-assembly-fulfillment-new-marketing-test-sales-sluggish-linuxmac-whats-next.html)。警告:Windows 版本需要。NET 3.5，下载[可再发行离线安装程序](http://www.microsoft.com/downloads/details.aspx?FamilyID=333325FD-AE52-4E35-B531-508D977D32A6&displaylang=en)，如果你不想让微软的在线安装程序访问互联网。

*使用它*

![breadboard](img/d8ef4a29689bb6259b2d1483e770c343.png "breadboard")

使用逻辑很简单。将灰色接地线连接到测试电路的地线，然后连接到您想要记录的信号线。我们将它连接到本周早些时候演示的 32K SPI SRAM。 [SPI](http://en.wikipedia.org/wiki/Serial_Peripheral_Interface_Bus) 有四个重要信号；使能、数据输入、数据输出和时钟。E-Z-Hooks 让接入信号变得非常简单，不会出现意外短路。

注意电线的方向。我们将黑线与地线联系起来，但逻辑电缆使用灰色。SparkFun 产品页面上的评论暗示，颠倒连接会破坏逻辑。

*![trigger](img/3d7192baf78b8fe0883034c23b3489b1.png "trigger")
*

该软件分析并显示信号捕获。主要配置选项是采样速率(200KHz-24MHz)和样本数量(数百万到数十亿)。我们能够以 24MHz 采样，但最高速度取决于有多少其他东西正在使用 USB 总线。24MHz 采样速率可以捕获高达 12MHz 的信号，我们发现这适合我们使用的所有协议。样本总数仅受可用 PC RAM 的限制。

有一个四个级别的触发器来监视信号，并在开始记录样本之前等待特定的组合。由于我们正在分析 SPI，因此开始捕捉的最合理位置是 SPI 使能信号在总线处理开始时下降。当 SPI 使能为 0 时，我们通过将其触发器更改为“0”来设置逻辑触发器开始采样。

![interp](img/86b18911892df1e5023cc32390643753.png "interp")

我们真的很喜欢解码最常见的串行协议的配置文件；单线、I2C、SPI 和异步串行。CAN 等协议[最终会加入](http://saleae.vox.com/library/post/1-wire-goodness-now-shipping.html)。

配置文件建议每个信号的名称，并将曲线转换成可读的字节值。这是一个非常棒的功能。如果没有它，你就必须计数时钟脉冲来识别字节边界，然后手动解码这些值。

该处理显示主机发出读取配置寄存器命令(0x05)和 SRAM 响应(0x41)。

![1-wire](img/40fba53bd546130f2ed34922daf1f490.png "1-wire")

我们还尝试了带有 [DS2431 EEPROM](http://hackaday.com/2008/12/24/parts-1k-1-wire-eeprom-ds2431/) 的单线解码器。软件识别单线复位命令和单线“搜索 rom”命令(0xf0)。

*一看里面*

*![insideii](img/065cc4e24d160196f82a1fc85f556168.png "insideii")
*

该逻辑基于 Cypress Semiconductor[cy7c 68013 a-56 pvxc](http://www.cypress.com/products/index.jsp?fid=14&rpn=CY7C68013A)，一种带有 USB 外设的英特尔 8052 微控制器。 [8052](http://en.wikipedia.org/wiki/Intel_8051#Related_processors) 是众所周知的 [8051](http://en.wikipedia.org/wiki/Intel_8051) 的加强版。我们还可以识别一个 24MHz 的晶体，它可能被内部的[锁相环](http://en.wikipedia.org/wiki/Phase-locked_loop)倍频到 48 或 96MHz。

*结论*

逻辑分析仪排除了调试芯片间通信的猜测工作。如果你看不到发生了什么，你最多只能猜测问题所在。当一个项目行不通时，99%的情况下，我们可以通过逻辑分析仪查看信号来立即解决问题。没有它，就无法知道发生了什么。

该逻辑以 24MHz 记录 8 个通道。Windows 软件有一些有用的功能，如果你想编写自己的应用程序，还有一个 SDK。Linux 和 Mac 版本正在开发中。我们真的很喜欢这个逻辑分析器，并计划用它来说明未来的文章。

逻辑是在 [Saleae 网站](http://www.saleae.com/logic/)和[spark fun](http://www.sparkfun.com/commerce/product_info.php?products_id=8938)149 美元，Joe 正在做欧盟分销。如果你对逻辑感兴趣，但不准备购买，你可以[下载软件](http://www.saleae.com/downloads/)并在演示模式下试用。

**Hack a Day review disclosure** :我们要求一个逻辑，Saleae 发给了我们