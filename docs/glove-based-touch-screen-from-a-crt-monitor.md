# 来自 CRT 监视器的基于手套的触摸屏

> 原文：<https://hackaday.com/2012/03/07/glove-based-touch-screen-from-a-crt-monitor/>

![](img/17e10c98f4a8898af22084a033b67752.png "glove-based-touch-screen")

这是一个笨重的旧 CRT 显示器，没有任何改动就被用作触摸屏。它不使用覆盖层，而是使用手套指尖的光电晶体管检测位置。

大多数基于 LCD 的触摸屏使用某种类型的覆盖层，[就像这些电阻传感器](http://hackaday.com/2011/10/28/the-basics-of-reading-data-from-resistive-touchscreens/)。但是阴极射线管显示器的工作方式与 LCD 屏幕完全不同，它使用电子枪和环形磁铁来引导电子束穿过屏幕。屏幕内部涂有荧光物质，当被电子激发时会发光。这个项目利用了这一特性，在手套指针和中指上都使用了光电晶体管。FPGA 驱动监视器并从传感器读取数据。它可以根据通过的电子束来推断光电晶体管在显示器上的位置，并将其用作光标数据。

休息之后，请观看视频，了解实际情况。它非常精确，但是我们确信这个系统可以从第一个原型开始变得更紧密一些。开发人员还提到，该系统在较暗的阴影下有一点麻烦。

[https://www.youtube.com/embed/HNXDjwqBhNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HNXDjwqBhNY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢卢克]