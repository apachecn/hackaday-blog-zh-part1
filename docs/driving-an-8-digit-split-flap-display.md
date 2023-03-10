# 驱动 8 位分割翻盖显示器

> 原文：<https://hackaday.com/2011/01/03/driving-an-8-digit-split-flap-display/>

![](img/e92706a631907296f2f1478c98c96903.png "split-flap-display")

[Markus]得到了一个分体式显示器，[为它制造了一个控制器](http://www.jave.de/blog2/?p=111)。这些有时可以在非常古老的闹钟上找到，但[Markus]是一只幸运的鸭子，设法获得了这个 8 位数的大显示器，它以前在一个火车站安家。它们的工作方式就像一个名片盒，在一个圆柱体上安装活板，形成完整的字母数字字体集。

选择 PIC 12F683 来控制显示器，使用光隔离将 42V 显示器电机与驱动电路分开。从休息后的视频来看，我们认为他做得很好。它只需要六个 I/O 引脚来控制，数字滚动的声音和外观让我们非常嫉妒。

那么他有什么打算呢？他做的第一件事就是用它来倒数新年。

[https://www.youtube.com/embed/HYhlQDS03KM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HYhlQDS03KM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)