# PSP 屏幕的 FPGA 驱动程序

> 原文：<https://hackaday.com/2009/12/12/fpga-driver-for-psp-screen/>

![](img/c59d8ddfe9a2ec4955ffd2e6e3737653.png "psp-screen-fpga")

朋友们不断给我们他们的旧电子产品。我们喜欢它，因为我们的垃圾箱是一堆永无止境的可能性。我们真的开始收集不容易连接的液晶显示屏，这个项目给了我们未来的希望。[Philip]已经发布了关于使用一个 [FPGA 作为替换 PSP LCD 屏幕](http://dsp-cg-fpga.blogspot.com/2009/09/welcome-this-is-my-blog-about-fpgas.html)的驱动程序。

许多[项目源手机液晶显示屏](http://hackaday.com/2009/09/28/capacitive-buttons-control-all-life/)有自己的驱动芯片，可以通过 SPI 寻址，与简单的微控制器配合使用。更复杂的屏幕需要更复杂的控制方案，这就是现场可编程门阵列接管的地方。[Philip]展示了他用来实现控制器的步骤，从设置正确的电压电平，到规划坐标寻址，甚至是他在反向电流方面的一些愚蠢行为。我们认为这将是向您介绍 FPGA 项目的一个很好的方式。