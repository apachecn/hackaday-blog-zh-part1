# LED 教程揭示了几种控制技术

> 原文：<https://hackaday.com/2012/03/08/led-tutorial-demystifies-several-control-techniques/>

![](img/9d0e6e72f0c1cf18e49abf10ad1ae606.png "LED_driving_and_controlling_methods_14")

控制 led 真的很简单。如你所知，它们需要限流，这就像将欧姆定律应用于给定的一组值一样简单。更重要的是，还有一系列恒流 LED 驱动芯片可以用来唱歌。但是你知道那些恒流电路是如何工作的吗？如果没有，那么[Giorgos Lazaridis '][LED 驱动和控制方法指南](http://www.pcbheaven.com/userpages/LED_driving_and_controlling_methods/)将带您快速上手。

他从最基本的概念开始，如何使用合适的限流电阻点亮 LED。但是从那以后，他开始了有趣的话题。他构建了一个基于晶体管的恒流驱动器，然后为电路增加了电压调节，如左图所示。他转到右边更鲁棒、更有效的方法，将 MOSFET 与晶体管电路配对。许多恒流驱动器的每个引脚都采用这种技术，无论电压输入电平如何，它都能正常工作。

他一直在制作视频来配合这些文章。休息过后，你可以观看左边示意图中的那一集。[https://www.youtube.com/embed/fMc99rM6u4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/fMc99rM6u4k?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[via [Reddit](http://www.reddit.com/r/electronics/comments/qlt9j/led_driving_and_controlling_methods/)