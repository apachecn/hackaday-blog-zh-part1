# 移除 Arduino 的外部振荡器以获得一对免费的 IO 引脚

> 原文：<https://hackaday.com/2012/03/22/remove-your-arduinos-external-oscillator-to-gain-a-free-pair-of-io-pins/>

![2free-arduino-io-pins](img/c28ae9882a21196ad79ea349f60ceffa.png "2free-arduino-io-pins")

来自 SpikenzieLabs 的[Mark]前几天使用 Arduino 完成了一个项目，发现自己需要更多的 I/O 引脚。他本可以在项目中增加额外的电路，但他决定看看是否可以通过移除一些元件来获得一些引脚。

他组装了一个 Minuino 板，但他没有安装晶体和相关的电容器，而是在它们的位置上添加了几个引脚。众所周知，芯片上的内部时钟不如晶体精确，但[Mark]的项目对时间并不敏感，因此他可以牺牲振荡器来获得一些额外的引脚。

有了新的 I/O 引脚，他只需要告诉 ATmega 芯片应该使用哪个时钟，就万事大吉了。虽然这可能不是所有项目的最佳解决方案，但是如果您正在构建重视 pincount 而不是 precision 的东西，这种方法非常适合您。

看看下面的视频，看看[马克]的黑客行动。

[via [HackedGadgets](http://hackedgadgets.com/2012/03/18/how-to-get-2-extra-pins-from-an-arduino/)

[https://www.youtube.com/embed/gHU0zrn1o-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/gHU0zrn1o-w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)