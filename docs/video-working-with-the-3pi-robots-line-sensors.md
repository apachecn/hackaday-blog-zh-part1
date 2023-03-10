# 视频:使用 3pi 机器人的线路传感器

> 原文：<https://hackaday.com/2011/11/12/video-working-with-the-3pi-robots-line-sensors/>

![](img/f79139cbfffb494f4f32540e96a15974.png "3pi")

本周，我们将进行系列的第五部分，使用 Pololu 3pi 机器人作为 ATmega328p 处理器的奇特开发板。本周，我们将暂时停止处理特定于处理器的外设，并展示如何处理 3pi 的线路传感器。快速浏览一下 3pi 的原理图，您可能会认为您应该使用 A2D 外设来读取线路传感器。即使它们被连接到 A2D 引脚，它们也需要被数字读取。在视频中，[Jack]将展示如何从传感器读取原始值，然后如何校准结果，以便您可以获得一个清晰的 8 位值，代表传感器看到的内容。当然，这在正常情况下是会发生的。墨菲在这个视频中有他的方式，结果是我们的演播室灯光干扰了我们拍摄时的传感器读数，所以我们没有得到我们拍摄时希望的那样好的校准。

视频在休息之后。

如果您错过了之前的视频，这里有一些链接:

第一部分:[设置开发环境](http://hackaday.com/2011/10/14/video-learning-to-program-for-the-atmega328p-part-i/)
第二部分:[基本 I/O](http://hackaday.com/2011/10/20/video-performing-io-with-the-atmega328p/)
第三部分:[脉宽调制](http://hackaday.com/2011/10/27/video-pwm-on-the-atmega328p/)
第四部分:[模数转换](http://hackaday.com/2011/11/03/video-analog-to-digital-conversion-on-the-atmega328p/)

[https://www.youtube.com/embed/9XjSJV5MPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/9XjSJV5MPc0?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)