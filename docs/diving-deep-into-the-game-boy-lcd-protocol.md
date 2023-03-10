# 深入研究 Game Boy LCD 协议

> 原文：<https://hackaday.com/2010/11/10/diving-deep-into-the-game-boy-lcd-protocol/>

![](img/647f2e01b64e1e59d1a4f6624a8ec88d.png "gnb")

[Craig]想让最初的 Game Boy LCD 屏幕为他服务，所以[他发现了它使用的数据协议](http://flashingleds.wordpress.com/2010/10/26/intercepting-the-gameboy-lcd/)。当他提到有一大群人把制造无意义的垃圾作为业余爱好的一部分时，我们被逗乐了。有罪。他接着概述了为什么这种液晶显示屏对业余爱好者来说是一个很好的资源。

从上面的引脚排列可以看出，它采用 5V 逻辑，数据时钟为 4 MHz。这些特性对各种廉价的微控制器都非常友好。如果你知道如何显示，应该很容易使用。此外，低引脚数得益于 4 色灰度屏幕，将数据引脚限制为两个。[Craig]连接他的 Saleae 逻辑探测器来捕捉通信，并向我们展示他的发现。在这个过程中，他向自己证明，他已经通过导出从逻辑探测器捕获的数据，并在他的计算机上将其重组为图像，弄清楚了协议。