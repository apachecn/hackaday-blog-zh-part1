# 如何用 PICkit 2 解码红外遥控信号

> 原文：<https://hackaday.com/2011/09/26/how-to-decode-ir-remote-control-signals-with-your-pickit-2/>

![](img/2d9ca430eeadedb81a3c731b0db3ff23.png "pickit2-IR-remote-control-decoder")

[SpiralBrain]需要弄清楚 IR 遥控器使用的编码方案，这样他就可以在自己的项目中使用它。他为 PICkit 2 建造了一个红外接收器板，并想出了如何使用一些微芯片软件来测量输入信号的时间。

硬件非常简单；一个 38 千赫的红外接收器通过过滤掉错误的红外光来完成繁重的工作。当检测到具有正确频率的信号时，输出引脚驱动晶体管的基极来触发 PICkit 2 上的输入引脚。分线板有一个引脚接头，可轻松拆卸和存放以备后用。PICkit 2 逻辑工具软件通过将正确的引脚设置为触发器并选择 10 kHz 采样速率来捕捉该输入。

正如我们在[我们的 Linux PIC 编程教程](http://hackaday.com/2010/11/03/how-to-program-pics-using-linux/)中所讨论的，PICkit 2 确实比它的替代品 PICkit 3 好得多。[SpiralBrain]提到它比新版本更通用，但没有告诉我们您是否可以在 PICkit 3 上使用该硬件。