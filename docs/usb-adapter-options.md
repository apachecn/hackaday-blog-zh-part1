# USB 适配器选项

> 原文：<https://hackaday.com/2010/09/16/usb-adapter-options/>

![](img/23a5692a7e3e2b0f715fbdcf659cb6a8.png "usb-serial-converters")

[Ladyada]抽出一些时间来解释通过 USB 连接项目的常用选项。你可能认为你已经用 Arduino 做到了这一点。嗯，是也不是。Arduino 使用这些选项中的一个，一个 FTDI 芯片，一边处理 USB，另一边发出微控制器友好的电压信号。这种芯片可以用于你的项目，这是一个[菲尔·伯吉斯] [详细介绍过的话题](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)。

在休息后的视频中，你还会听到 USB 到串行转换器，它连接到通用串行总线并输出传统的 12-20V 串行信号(除了像上周一样的[廉价山寨电缆)。需要使用 MAX232 芯片将这些电压降低到 5 伏或更低，以配合您的项目。](http://hackaday.com/2010/09/11/cheap-cable-reused-to-add-usb-to-your-project/)

最后，可以选择使用运行 [V-USB 固件包](http://www.obdev.at/products/vusb/index.html)的微控制器。这就是 [USBtinyISP](http://www.ladyada.net/make/usbtinyisp/) 的工作方式，我已经在自己的项目[中使用它来构建一个兼容 LIRC 的红外接收器](http://jumptuck.com/?p=20)。

[https://player.vimeo.com/video/14980412](https://player.vimeo.com/video/14980412)

[感谢 PT]