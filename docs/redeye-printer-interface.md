# 红眼打印机接口

> 原文：<https://hackaday.com/2011/04/05/redeye-printer-interface/>

![](img/e1ac1909340dee4dd58499a0f506fa7c.png "IMG_0254")

这个[便捷的打印机接口](http://www.wire2wire.org/HP82240B_adapter/HP802240B_adapter.html)最初是我们自己的[论坛](http://forums.hackaday.com/viewtopic.php?f=10&t=427&sid=313b60966d50c458c78ac0abaac3aae6)上的一个请求，当时论坛成员【victorf】需要通过热敏打印机进行一些输出。他已经获得了许多 HP82240B 热敏打印机的分数，这些打印机旨在与 HP 计算器一起使用，但当然它们使用的是 20 世纪 60 年代首次起草的有点神秘的 HP 协议，需要一些帮助。

论坛成员[wireb]开始研究它，发现它使用标准的 32KHz 载波信号，并开始询问它的用途。抓住一个 pdf 的手册，他能够找出所有的细节，什么是打印机期待的通信形式。

几周后，[wireb]能够基于 PIC16F1824 制造一个方便的逻辑级串行转 HP-IR 适配器，pic16 f 1824 的固件支持 9600 8N1 或 2400 8N1 速度、ASCII 文本和打印机通过转义序列的“高级”图形模式。

如果您还没有查看我们的[论坛](http://forums.hackaday.com/)，我们建议您查看！