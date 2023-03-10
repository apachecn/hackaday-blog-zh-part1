# 使用平行 WAV 屏蔽将弹球音频分层

> 原文：<https://hackaday.com/2011/02/27/layering-pinball-audio-using-parallel-wav-shields/>

![](img/e1f794b555cc0a27d3355e8098a1ce4a.png "parallel-arduino-audio")

[Ed Zarick]正在准备他的弹球项目，并希望有真实的声音来配合游戏。这个游戏是模仿 NBA Hangtime 的，除了音乐之外，他还需要各种各样的音效来增强体验。为了让这一切同时发生，他开发了一套由 Arduino Mega 控制的 Arduino WAV 防护罩。

正如你在上面看到的，有三个 ATmega328 芯片运行 Arduino 引导加载程序，每个接口都有三个绿色 WAV 盾中的一个。这组芯片通过 i2c 协议监听命令，一旦它们收到指令，它们就可以播放选定的文件，而不会影响其他屏蔽。

但是要获得真实的声音，你首先需要获取音频样本。[Ed]拿了一个原始视频游戏的 ROM，并丢弃了所有的音频样本。从那以后，用弹球版的游戏来听声音和给 SD 卡播放的声音分类就成了一件苦差事。但是这种努力是值得的，因为声音最终会将整个体验联系在一起。

[https://www.youtube.com/embed/tEI5F_lRd6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/tEI5F_lRd6Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)