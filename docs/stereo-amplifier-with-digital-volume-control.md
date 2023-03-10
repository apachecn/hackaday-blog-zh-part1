# 带数字音量控制的立体声放大器

> 原文：<https://hackaday.com/2011/06/27/stereo-amplifier-with-digital-volume-control/>

![](img/1923ac524ba7c2a35d477e9d7820786b.png "CircuitSetup1")

一个定期的 Hack A Day 读者发送了一个关于带数字音量控制的 LM386 stero 放大器的提示。最终的构建非常专业，可以很容易地改编成一个光滑的 iPod dock 构建。

这些年来，我们已经看到了一些基于 LM386 的放大器，包括安装在 9V 电池内的[放大器](http://hackaday.com/2010/02/03/amplifier-built-inside-a-9v-battery/)，但这是我们看到的第一个数字控制音量的实现。这个放大器的音量控制使用 [DS1868 双数字电位计 IC](http://www.maxim-ic.com/datasheet/index.mvp/id/2810) 代替通常的 10K 电位计，提供零到满音量之间的 256 步。DS1868 由一个带三线串行连接的 PIC μC 控制，尽管这可以在任何微控制器上实现。

虽然这个版本提供的代码将音量输出为线性函数，但是实现对数音量输出是微不足道的。因为耳朵[以对数标度](http://en.wikipedia.org/wiki/Fletcher%E2%80%93Munson_curves)感知响度，这将是调节音量并提供更细粒度控制的一个好方法。当然，这可以用对数锅来实现，但这有什么意思呢？

休息之后，请观看放大器的视频。

[https://www.youtube.com/embed/O38PZX__r4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/O38PZX__r4g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

