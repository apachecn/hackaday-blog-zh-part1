# 示波器兼作串行终端

> 原文：<https://hackaday.com/2010/02/24/oscilloscope-doubles-as-a-serial-terminal/>

![](img/b87b879fe44c126707fea2d5c48b65d5.png "Terminalscope")

基于 PC 的 USB 示波器正迅速风靡一时。【马特·萨诺夫的】*终端示波器*采取相反的方法，[将示波器改装成全串行终端](http://www.msarnoff.org/projects/terminalscope/)。你可能以前在 Dutchtronix/spark fun[O-Clock](http://www.sparkfun.com/commerce/product_info.php?products_id=9306)中见过类似的东西，但是【Matt 的】项目更进一步，增加了一个 [PS/2 键盘](http://hackaday.com/2009/09/29/connect-a-ps2-keyboard-to-a-microcontroller/)端口，用于完全双向[串行](http://hackaday.com/2010/02/23/serial-communication-with-cell-phones/)通信，并且具有更清晰的显示分辨率。

主要兼容 VT-100 的终端示波器是围绕两个 [AVR](http://hackaday.com/2010/02/10/the-day-after-arduino/) 微控制器构建的:一个 [ATmega328P](http://hackaday.com/2010/02/16/the-mini-markade/) 全速运行以生成视频信号并处理串行 I/O，而一个 [ATtiny45](http://hackaday.com/2008/04/01/random-usb-caps-locker/) 处理键盘输入以避免中断‘328’的任务。不是矢量跟踪每个字符，而是使用光栅扫描方法:光束沿着固定的 X/Y 路径(像电视一样)，同时调制 Z 输入(光束强度)以形成图像。该设备可以通过串行端口或 [USB 转 TTY 适配器](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/)连接到 PC，或者直接连接到另一个微控制器以调试串行输出。

我们最近展示了一个被用作[多通道数字逻辑显示器](http://hackaday.com/2010/02/11/use-an-analog-oscilloscope-to-display-digital-logic/)的示波器。Terminalscope 为这个基本的工作台工具提供了[的另一个用途](http://hackaday.com/2008/07/16/tennis-for-two-resurrected/)，可以很好地完善一个“穷人的”测试设置。原理图和完整的源代码可以下载。