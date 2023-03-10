# 使用 BeagleBone 暴力破解受密码保护的 PDF

> 原文：<https://hackaday.com/2012/03/26/brute-force-a-password-protected-pdf-using-the-beaglebone/>

![](img/0dc158d8205576fd4689a7e13ab2f0f1.png "hardware-pdf-password-cracker")

使用 BeagleBone 的最大好处是它的 700 MHz ARM 处理器。如果你只是在摆弄基本的 I/O，这种能力是没有用的，但[努诺·阿尔维斯]正在利用它的能力。他基于 85 美元的开发板构建了[一个 PDF 密码破解程序。](http://www.nunoalves.com/open_source/?p=221)

我们最近看到使用 BeagleBone 执行[基本 I/O 是多么容易。这些技术在这里发挥作用，用来驱动一个字符液晶显示器，并从试验板电路采样按钮输入。[Nuno]甚至为这些外围功能分别发布了帖子。](http://hackaday.com/2012/03/15/twiddling-an-led-using-the-beaglebones-embedded-linux/)

受密码保护的 PDF 文件通过拇指驱动器传送到设备。因为 BeagleBone 运行的是嵌入式 Linux，所以你不需要考虑如何从设备上读取数据。点击按钮启动该过程。目前，该代码仅使用暴力攻击，每秒钟可以测试 6000 多个四字符密码。对于任何长度超过四五个字符的密码来说，这都非常慢，但[Nuno]确实提到了并行运行几个 ARM 处理器的可能性，或者使用字典(或彩虹表)来加快速度。不管怎样，在硬件上尝试都是一个有趣的项目。休息之后你可以看到他的视频演示。

[https://www.youtube.com/embed/1uXesJL-hok?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1uXesJL-hok?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)