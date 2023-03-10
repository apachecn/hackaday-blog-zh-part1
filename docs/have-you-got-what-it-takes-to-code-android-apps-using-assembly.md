# 你知道用汇编语言编写 Android 应用程序需要什么吗？

> 原文：<https://hackaday.com/2011/09/15/have-you-got-what-it-takes-to-code-android-apps-using-assembly/>

![](img/183a73c86458c597117213b894b38708.png "android-assembly")

你有一个根 Android 设备和一台运行 Linux 的电脑吗？如果是这样，你已经在用汇编语言为 Android 编码的路上了[。Android 设备使用 ARM 处理器，而[Vikram]认为 ARM 提供了最不复杂的汇编平台，使其成为汇编编程新手的绝佳选择。我们认为他的八部分教程很好地介绍了这种语言，并解释了如何启动和运行开发工具。你需要知道一些基本的编程概念，但是从我们看到的来看，你不需要任何 ARM 或 Android 的经验。](http://www.eggwall.com/2011/09/android-arm-assembly-device-set-up-part.html)

那么，为什么要学习汇编呢？几个月前，我们尝试了 AVR 的汇编语言，[真的学到了很多关于硬件](http://hackaday.com/2011/07/09/hardware-xor-for-output-pins-on-avr-microcontrollers/)的知识，而我们从来不需要知道用 c 编写。这是优化函数的一个很好的方法，因为高级语言编译器的怪癖会浪费太多时间。这意味着您不需要用汇编语言编写整个应用程序。您可以简单地使用它来简化代码中复杂的部分，然后在编译时包含那些汇编文件。