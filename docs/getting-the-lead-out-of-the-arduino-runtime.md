# 从 Arduino 运行时中获得领先优势

> 原文：<https://hackaday.com/2011/10/01/getting-the-lead-out-of-the-arduino-runtime/>

![mhvlib_arduino_efficiency_runtime](img/916c30355884605edfe7b198fe8b2f93.png "mhvlib_arduino_efficiency_runtime")

啊，阿尔杜伊诺。

不管你喜欢它还是讨厌它，不可否认的是，它的易用性是以牺牲速度和效率为代价的。我们真诚地喜欢这个平台以及所有其他的平台，因为我们相信每样东西都有它合适的位置和目的。Make、Hack、Void 的工作人员认为 Arduino 开发板很好，但是 Arduino 运行时的核心需要一些改进。

他们主动深入研究代码，做出了一些许多高级 Arduino 用户一直渴望的改进。他们的 MHVLib 是一个面向效率的运行时库，可在所有 AVR 微控制器上运行，无论是独立的 uCs 还是 Arduino 品牌的硬件。

它们改变了 Arduino 处理 pin 和端口信息的方式，以及对象和缓冲区在内存中的分配方式。他们的代码仍然依赖于 Arduino 风格的引导加载程序，尽管他们推荐 [Optiboot](http://code.google.com/p/optiboot/) ，因为它的大小大约是 Arduino 版本的四分之一。

在他们的网站上有一个已经实现的完整列表，如果你想自己尝试一下，你可以通过他们的 GIT 库获取代码。