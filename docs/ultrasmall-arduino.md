# 超小型 Arduino

> 原文：<https://hackaday.com/2011/02/21/ultrasmall-arduino/>

![](img/f6baa945070bc02e5f03cff7015c77bf.png "Image426")

[Fabio vares ano]新的 Arduino 兼容板在超紧凑的布局中实现了强大的功能，尺寸为 20.7×15.2 毫米， [Femtoduino](http://www.varesano.net/projects/hardware/Femtoduino) 可能是目前最小的基于 328 的 Arduino 兼容板。大部分的钉书钉都在，一个 QFN atmega328，一个 [MIC5205](http://www.micrel.com/_PDF/mic5205.pdf) 适用于几百毫安的低压差稳压器，16MHz 陶瓷谐振器，复位，电源指示器和 13 针 led，但是你需要提供你自己的串行连接(FTDI，MAX232 等)和另一个 AVR 编程器来将 Arduino 引导加载程序加载到芯片上。

由于电路板很小(比 pro mini 更小)，它不是直接的试验板友好型。尽管孔的间距是 0.05 英寸，但对于“普通”电线来说，这个尺寸已经足够大了，如果你想使用 0.1 英寸的间距，你可以在 Femtoduino 刚刚咬合的地方制作一个方便的分线板。

制作您自己的电路板所需的一切都在网站上提供，原理图、kicad 文件、物料清单、用于电路板和分线板的 Gerbers，尽管我们希望尽快看到这是一个预制电路板，请在休息后加入我们，观看视频并了解原因。

[https://www.youtube.com/embed/w-TVLYRprAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/w-TVLYRprAI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)