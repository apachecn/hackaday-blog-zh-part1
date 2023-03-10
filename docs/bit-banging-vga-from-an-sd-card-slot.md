# 从 SD 卡插槽对 VGA 进行位碰撞

> 原文：<https://hackaday.com/2011/05/10/bit-banging-vga-from-an-sd-card-slot/>

![](img/f631d0b7c389248f29e6f3edcab16de8.png "bit-banging-vga")

如果你有一些喜欢的电子设备，包括 SD 卡插槽，但没有视频输出端口，你可以通过读卡器导线推送 VGA 信号。这正是上面 Ben NanoNote 的情况，这是一款[低于 100 美元的 Linux 设备](http://hackaday.com/2010/03/28/hackaday-links-march-28-2010/)，我们以前见过[将其 SD 卡插槽用作通用 I/O](http://hackaday.com/2011/02/20/rf-control-from-just-about-any-device/) 。

捕捉信号的硬件包括用于卡插槽的分线板。连接器卡的另一端是一组自由形成的电阻，用于处理 VGA 颜色信号的电平转换，并通过 VGA 电缆连接到显示器。造成这种情况的软件是一个肮脏的黑客，它在显示静止图像时阻止所有其他功能。但是我们确信它可以被清理干净。只是不要对全动态视频抱太大希望，这个小家伙就是没有这种能力。

【经由[危险原型](http://dangerousprototypes.com/2011/05/09/bitbang-vga-from-an-sd-card-slot/)经由[斜线](http://hardware.slashdot.org/story/11/05/07/1215246/Micro-SD-Card-Slot-Abused-As-VGA-Port)