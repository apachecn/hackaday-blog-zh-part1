# 与 PS/2 键盘接口

> 原文：<https://hackaday.com/2011/09/23/interfacing-with-a-ps2-keyboard/>

任何阅读这篇文章的人无疑都使用过键盘。然而，它们的工作方式比“一个按钮，一个输入”要复杂一些【PyroElectro】有一个[很棒的教程](http://www.pyroelectro.com/tutorials/ps2_keyboard_interface/)关于用 7 段 LED 显示屏搭建 PS/2 键盘接口(休息后视频)。教程背后也包含了相当多的理论。

下面显示的系统使用 PIC 控制器来显示按下的字母或数字。这里给出了整个项目的示意图以及详细的[物料清单](http://www.pyroelectro.com/tutorials/ps2_keyboard_interface/parts.html)。

至于 PS/2 键盘是如何工作的，每一次[击键都被编码](http://www.pyroelectro.com/tutorials/ps2_keyboard_interface/theory_ps2.html)成一个二进制数或者“扫码”。这些代码大多数是 8 位的，但是一些特殊的符号使用更长的代码。虽然这篇文章没有完全解决这个问题，但是可以使用一种非常类似的方法将数据发送回键盘，例如调整“capslock”或“numlock”键。虽然开灯很有趣，但我们可以看到这是一种出于自动化目的控制继电器的权宜之计。

 [https://www.youtube.com/embed/W2c2NXV7gD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/W2c2NXV7gD0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)