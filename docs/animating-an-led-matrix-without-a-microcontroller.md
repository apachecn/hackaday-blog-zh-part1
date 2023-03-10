# 无微控制器的 LED 矩阵动画

> 原文：<https://hackaday.com/2011/02/09/animating-an-led-matrix-without-a-microcontroller/>

![](img/c83e0a3bb1f44156bf5fe190c5726408.png "animating-led-matrix-without-microcontroller")

[Konstantin]有一些额外的 27C256 EPROMS，并且[决定用它们来制作一个 8×8 的 LED 矩阵](http://www.konstant.in/?p=277)。他不仅用它们来存储数据，还用它们来驱动显示器。该芯片拥有 32 千字节的数据，相当于 4096 帧动画。一个 32 kHz 的时钟电路与一些纹波计数器一起工作，滚动存储数据的每个字节，打开列，同时吸收适当的行。当然，电流保护是必须的，因此有一个 ULN2308A 达林顿驱动器和一些 2N2907 晶体管在工作，但你不会找到可编程微控制器。整洁！

是的，你没看错。上图显示了一个 EPROM 芯片，[需要一个紫外光源来擦除](http://hackaday.com/2010/10/21/uv-eprom-eraser-in-a-toolbox/)数据。

[谢谢你的头猴子]