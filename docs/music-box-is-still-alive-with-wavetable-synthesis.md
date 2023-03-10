# 音乐盒仍然与波表合成活着

> 原文：<https://hackaday.com/2012/01/17/music-box-is-still-alive-with-wavetable-synthesis/>

![](img/43052b9046296e168d39e2ca2b819939.png "pic")

尽管美妙的音调来自一个百年的音乐盒，我们不得不承认[Markus]'[wave table synthesis build](http://dangerousprototypes.com/forum/viewtopic.php?f=56&t=3472)仍然令人印象深刻。当然，通过做*仍然活着*的演示而获得的网络信誉也有所帮助。

[波表合成](http://en.wikipedia.org/wiki/Wavetable_synthesis)在 RAM 中存储一个周期长的波形，可以以不同的频率循环播放。这种技术自 70 年代末就已经出现，可以在 80 年代的许多经典合成器中找到，并作为 Atari MOD 音乐和由[小声音 DJ](http://littlesounddj.com/lsd/) 制作的 Game Boy chiptunes 的基础

[Markus]发现了一对电池供电的笔记本电脑扬声器，并认为音乐盒将是一个很好的项目。受[ChaN]的[at tiny 波表合成器](http://elm-chan.org/works/mxb/report.html)的启发，[Markus]决定加大赌注，使用 PIC32 微控制器使编程更容易理解。整个项目(有一个可怕的死虫焊接工作)几乎和图片本身一样大。

[Markus]抛出了源代码和一些 Python 脚本，将波形和 MIDI 文件转换成芯片可以理解的东西。在你检查之前，一定要看一下*仍然活着*的演示。

[https://www.youtube.com/embed/dt3rpgWyKno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dt3rpgWyKno?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)