# 带电视输出的 CV 音序器

> 原文：<https://hackaday.com/2011/09/27/cv-sequencer-with-a-tv-out/>

![](img/bc2e3d4f08f7b3481ba527212ba2198b.png "synth")

[gijs]发送了他一直在研究的[控制电压序列发生器](http://gieskes.nl/instruments/?file=tvscv),它使用 TVout Arduino 库来提供图形界面。

音序器本身不会发出任何声音。相反，它输出一个控制电压，以便其他合成器可以用[gijs]' TVSCV 排序。在 MIDI 出现之前，CV 是连接合成器和鼓机的标准。即使在今天，许多精品合成器至少有一个 CV 插孔。[gijs]“构建非常有趣，因为它的用户界面——[TV out Arduino 库](http://code.google.com/p/arduino-tvout/)与一个微型 CRT 结合使用，以改变 CV 输出的值、定时和速度。TVSCV 能够以 10 位分辨率对 CV 的两个不同通道进行排序，每组 16 步。

从休息后的视频来看，TVSCV 听起来像是可以为雅达利或 NES 游戏制作出最令人神往的配乐。这是一个很棒的套件，特别是当连接到雅达利朋克游戏机或 TR-808 和小故障延迟时。

[https://www.youtube.com/embed/HJaivnrdqU4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HJaivnrdqU4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)