# 欧姆感测可以感知电阻色带

> 原文：<https://hackaday.com/2011/08/06/ohm-sense-makes-sense-of-resistor-color-bands/>

[![](img/da7d0f69a86b3a80c50483c02373a3c6.png "phone")](http://hackaday.com/wp-content/uploads/2011/08/phone.png)

[Alex Busman]在 iOS 编程方面的首次尝试看起来是一个非常有用的工具。他开发了一款名为 [Ohm Sense](http://itunes.apple.com/us/app/ohm-sense/id453570510?ls=1&mt=8) 的 iPhone 应用程序，它可以拍摄一张电阻的照片，并根据色带计算电阻值。这是一个伟大的工具，我们希望我们有当我们开始了。这款应用售价 99 美分，比我们和紫罗兰(T3)之间的[情感成本要便宜得多。](http://en.wikipedia.org/wiki/List_of_electronic_color_code_mnemonics)

【Alex】使用 [OpenCV](http://opencv.willowgarage.com/wiki/) 对图像数据进行处理。该应用程序的工作原理是从左上角扫描图像，直到看到一个米色的矩形。在电阻器周围画一个边界框后，iPhone 会扫描图像中的颜色列。稍微解释一下，屏幕上就显示出了电阻值。虽然它现在只对米色塑料电阻器有效，但[Alex]说他将来会将它扩展到蓝色金属氧化物电阻器。[Alex]说编码只花了一周时间，所以如果有人想为 Android 编写类似的应用程序，请务必在我们的[提示热线](http://hackaday.com/contact-hack-a-day/)上告诉我们。

这不是[Alex]第一次一天黑一次。今年夏天早些时候，我们特别介绍了他的 [Handy Board 项目](http://hackaday.com/2011/06/28/handy-board-plays-music-with-an-nes-controller/)，该项目使用一个 NES 控制器来演奏一些芯片曲调。与我们过去几个月错过的项目相比，很高兴看到*有人*在他们的夏天做了一些有成效的事情。

[Alex]在 YouTube 上发布了他的电阻应用程序的演示。下面来看看吧。

[https://www.youtube.com/embed/Nk0AEv8825U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Nk0AEv8825U?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)