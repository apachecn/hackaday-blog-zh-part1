# 老式 VT100 终端计算……带猎兔犬骨

> 原文：<https://hackaday.com/2012/03/07/vintage-vt100-terminal-computing-with-a-beaglebone/>

![decbox](img/9a3dc3ab44102275c3af9df835888a89.png "decbox")

一个很酷的小项目摆在我们面前，我们认为你们中的一些老式电脑爱好者可能会感兴趣。[Joerg Hoppe]来信分享了他以新颖的方式复活的 DEC VT100 终端。

由于 SIMH 项目，他的“DECBox”系统是用 Beaglebone 创建的，他用它来运行各种 PDP11/VAX 终端仿真器。【Joerg】为 Beaglebone 建造了一个扩展屏蔽，提供几个 UART 连接，使他能够通过串行接口将其连接到他的 DEC 终端。由于他在 Beaglebone 上添加了几个串行插头，他甚至可以在不同的终端上并行运行多个仿真器安装，而不会有太大的麻烦。

[Joerg]的努力主要是为了他正在建造的老式计算机显示器，但建立这样一个自己的系统应该没有问题。如果您碰巧有一个(或多个)这样的盒子在收集灰尘，这将是一种无需庞大的外部硬件即可让它们全部启动并运行的简单方法，因为 Beaglebone 可以很好地嵌入 VT100 的后部扩展槽中。

请务必查看他的网站，了解更多关于他的 DECBox 软件包如何工作的细节，以及更多复古终端的图片。