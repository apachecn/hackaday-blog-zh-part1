# 准系统 PIC RFID 标签

> 原文：<https://hackaday.com/2011/09/26/barebones-pic-rfid-tag/>

![](img/c6a259b5ef8b1ebcb59036f6ea184c0a.png "barebones-pic-rfid-tag")

一个感应器和 8 针微控制器组成了这个准系统 RFID 标签。当你第一次看到上面的图片时，你可能会大吃一惊。毕竟，芯片上没有任何东西连接到电源和接地引脚。正如[拉米罗·帕雷贾]在他的帖子中解释的那样，电源实际上是通过电感焊接到的 I/O 引脚提供的。似乎每个 I/O 引脚在芯片内部都有一个寄生电容和一对箝位二极管。当 RFID 阅读器磁场感应的交流电流到达这些引脚时，电容充电，箝位二极管形成桥式整流器。这导致功率被注入芯片，芯片转过身来，通过电感发送回 RFID 代码。

这不是我们第一次看到这个概念。我们展示了一个完全相同的黑客，除了[它使用了 AVR 芯片](http://hackaday.com/2009/06/27/avr-rfid-tag/)。这一个使用 PIC 12F683，但是应该与任何 12F 或 16F 模型一起工作。代码是用汇编语言编写的，不需要为不同的硬件做任何改动。[Ramiro]确实谈到了为 Vss 和 Vdd 增加一个去耦电容，以及为上面使用的两个 I/O 引脚增加一个调谐电容，以帮助提高器件的鲁棒性。但是，正如你在休息后的视频中看到的，没有他们也能很好地工作。

[https://www.youtube.com/embed/JiHc_hI5NAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/JiHc_hI5NAw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢难题]