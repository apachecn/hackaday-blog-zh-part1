# 安卓说话脉冲波

> 原文：<https://hackaday.com/2010/11/10/android-talks-pulsewave/>

![](img/9f4b6f2fe28740224764fbae286d9bcc.png "Picture 2")

串行通信是数字计算的支柱。它们不需要太多的物理基础设施，并且它们以各种形式存在，以适合几乎任何应用。串行通信线路的行为类似于 1 位 DAC，以定时模式从高电压变化到低电压。在大多数情况下，使用整个 DAC 进行串行通信是一种浪费，但是[[robot every where](http://www.robots-everywhere.com/)团队发现了一个例外，你可能已经遇到了。

由于机器人的音频输出是可访问和可寻址的，[ [RobotsEverywhere](http://www.robots-everywhere.com/) ]编写了源代码，将左右声道用作独立的串行通信线路。这避免了闯入设备和摆弄硬件的需要，如果你想要一个允许 RS232 端口通信的无风险黑客，这是很好的。任何可以写入 DAC(并控制采样速率)的硬件都是潜在目标。

需要一些外部电子设备来将音频信号转换为 TTL，但这并不复杂，只需几个比较器和转换器。休息之后你可以看到它的实际效果。

作为奖励，当你结束一天的工作后，你可以插上耳机，听一整晚的脉搏波舒缓的诗歌。

[https://www.youtube.com/embed/PfSSPTtacnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/PfSSPTtacnk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)