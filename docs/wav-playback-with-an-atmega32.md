# 使用 ATmega32 播放 WAV

> 原文：<https://hackaday.com/2012/02/29/wav-playback-with-an-atmega32/>

![](img/5f9d9ad26213ca9554af32d6638826bf.png "microcontroller-based-wav-audio-player")

[Vinod Stanur]刚刚完成了另一个业余爱好项目，他使用微控制器构建了一个 WAV 音频播放器。不久前，他开始使用 PIC 微控制器进行开发。但是他使用的芯片没有足够的 SRAM 来分配作为播放缓冲区。当他拿到一台 ATmega32 时，他的注意力又回到了这个项目上，并且一直看到了结束。

他利用了他在几个早期构建中所学到的东西。他使用电视遥控器作为输入，就像他的贪吃蛇游戏一样。存储由 MMC 卡提供，这是他在[这个录音机项目](http://hackaday.com/2011/09/03/pic-based-voice-recorder/)中完善的一个技巧。他没有使用 FAT 库，而是使用自己的代码来读取扇区地址的链表(文件分配表),然后解析 WAV 头并相应地处理文件。

回放使用两个 512 字节的缓冲区。一个是馈入输出，而另一个是从存储卡填充。当输出缓冲器耗尽时，两者交换，过程继续。休息之后你会看到[Vinod 的]项目演示。

[https://www.youtube.com/embed/YMlm4ycDDKI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YMlm4ycDDKI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)