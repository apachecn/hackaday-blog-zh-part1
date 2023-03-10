# 用 Arduino 轻画 Nyan 猫

> 原文：<https://hackaday.com/2011/10/21/light-painting-nyan-cat-with-an-arduino/>

![](img/84ad8b21a5731b92bd0e9ae442880db7.png "arduino-light-painting")

你也可以用一些工具来描绘你最喜欢的迷因。[Skywodd]汇集了几个不同的项目来实现这一目标。他已经建造了一个大型视点显示器，现在[使用长曝光的 DSLR 来创作光绘](http://arduino.cc/forum/index.php/topic,72711.0.html) ( [翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Farduino.cc%2Fforum%2Findex.php%2Ftopic%2C72711.0.html))。

Arduino 供电的显示器由 35 个 RGB LEDs 组成。现在，每个 LED 有四个引脚，但其中一个接地，只剩下 105 个引脚需要寻址。有几件事使这变得易于管理。首先，他为 LED 灯条蚀刻自己的电路板。这样可以断开电路板边缘的触点，并通过处理接地总线来简化焊接。其次，他使用 M5450 LED 显示驱动器进行寻址。休息之后，你可以看到原型硬件的视频(法语，但 blinky 行动大约在 2:30 开始)。

如果你正在寻找一种更简单的方法来做到这一点，看看使用人造 LED 条的[光绘。](http://hackaday.com/2011/07/11/led-wand-for-light-painting-photography/)

[https://www.youtube.com/embed/e8mazjpXHzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/e8mazjpXHzI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)