# 临时构建的软件定义无线电

> 原文：<https://hackaday.com/2011/12/21/scratch-built-software-defined-radio/>

![](img/466d8afea29fa0a92fcd14b86ca9092f.png "software-defined-radio-project")

[Ben]正在展示他的软件定义无线电项目的一些成果。上面看到的板子，是他从头开始设计的，正在接收 WWV 电台的广播。这是来自科罗拉多州柯林斯堡的原子钟信号。休息后在剪辑中听到的音频有点嘈杂，但由于他距离信号的来源大约 2000 英里，我们认为他做得非常好！

早在 7 月份，当他看到[Jeri ells worth]的[SDR 项目](http://hackaday.com/2011/07/19/jeri-ellsworth-builds-a-software-radio/)时，这种构建的种子就在[Ben]的脑海中播下了。他在[的一个论坛帖子](http://nbitwonder.com/forum/viewtopic.php?f=20&t=52)上发布了一些建造细节。这种方法与[Jeri 的]相似，但有几个关键的区别。他使用的是 DS1085 可编程振荡器，她为此选择了 FPGA。一旦他的硬件对输入信号进行解调和滤波，PIC32 就会完成剩下的工作，并向运算放大器输出 PWM 信号以产生音频。

[https://www.youtube.com/embed/dWnyZbn06qw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dWnyZbn06qw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)