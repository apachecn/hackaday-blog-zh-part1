# 不用微控制器录音

> 原文：<https://hackaday.com/2011/09/15/record-sound-without-a-microcontroller/>

![](img/0db021cb71681ba7d3a7a1e388718a72.png "breadboards")

为了他的 A-level 电子课程工作，[Andrew]决定建造一个不使用微控制器的数字录音机。

[Andrew]的构建以 8000 样本/秒的速度从板载麦克风捕获音频。音频被数字化成 8 位声音数据并发送到 SRAM。记录和回放功能完全由 4000 系列逻辑芯片控制。他承认音质相当差；这主要是由于 8kHz 的采样速率。[然而，在某些圈子](http://www.youtube.com/watch?v=pomqDMUnT60)中，糟糕的采样率被认为是非常酷的，所以我们不会说[Andrew]的构建是无用的。

[Andrew]的设计中有一些非常聪明的设计选择，比如麦克风上的截止滤波器设置为 4000 Hz(他的系统的奈奎斯特频率)。对于记录媒体，他使用了一个 SRAM，可以保存大约半兆字节的数据。在 8000 样本/秒的速度下，[Andrew]的版本可以存储 60 秒多一点的音频。这个建筑可能不是一台逻辑芯片计算机，但毫无疑问，安德鲁学到了一些东西。点击查看【安德鲁】66 页的课程报告[(PDF 警告)。](http://hackaday.com/wp-content/uploads/2011/09/electronics2.pdf)