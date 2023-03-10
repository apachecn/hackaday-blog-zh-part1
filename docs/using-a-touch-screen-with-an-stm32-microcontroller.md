# 使用带有 STM32 微控制器的触摸屏

> 原文：<https://hackaday.com/2012/01/10/using-a-touch-screen-with-an-stm32-microcontroller/>

![](img/09efd23e6507bce7c738b0478658a500.png "stm32plus-touch-screen")

[安迪·布朗]一直致力于围绕 STM32 处理器系列的一系列教程。他使用 STM32plus 开发板和 STM32F1 ARM Cortex M3 处理器来驱动几个不同的全彩色图形 LCD 屏幕。他的最新作品展示了[如何从两个显示器附带的触摸屏](http://andybrown.me.uk/ws/2012/01/07/stm32plus-ads7843-touch-screen-driver/)上阅读。

休息过后，我们嵌入了截图中的视频。例如，[Andy]编写了一个绘画程序来展示触摸屏的功能。它从我们都熟悉的校准程序开始，然后下降到这个带有虚拟控制面板和空白画布的屏幕。

这种硬件使用德州仪器的 ADS7843 控制器，Andy 说这种控制器非常常见，其他几家制造商也使用相同的通信协议。他讨论了如何与控制器通信，以及如何将数据合并到您的程序中。包括一个开源库，您可以在自己的项目中使用。

[https://www.youtube.com/embed/0Sv9fKLKvKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/0Sv9fKLKvKc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)