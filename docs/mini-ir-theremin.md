# 迷你红外特雷门琴

> 原文：<https://hackaday.com/2011/07/08/mini-ir-theremin/>

![](img/49ed41637684aa973af5eda8bc272fda.png "theremin")

PyroElectro 公司的[Chris]发来了一份关于微型红外 theremin 的 8 部分的精彩报道。

特雷门是基于 PIC 微控制器和红外距离传感器。构建日志详细介绍了 [IR 传感器](http://www.pyroelectro.com/projects/mini_ir_theremin/ir_sensor_theory.html)和[音调生成](http://www.pyroelectro.com/projects/mini_ir_theremin/speaker_tone_theory.html)的工作原理。[Chris]在展示设计中的数学方面做得非常好。

虽然这个项目不是真正的特雷门琴，因为它像我们过去报道过的其他项目一样依靠光来操作，但由于硬编码的音符，它更容易演奏。不过，这种构建确实展示了一些前景——他可能会扩展它，使用更精确的超声波传感器，或者使用“两个接近传感器，一个用于高音，一个用于低音，就像手风琴一样。”

特雷门琴通常用双手演奏[，提供连续的音高和音量。这个项目以硬编码的离散音符为特色，所以我们想知道在这个 IR theremin 上实现 MIDI 的可能性。最初的](http://www.youtube.com/watch?v=Bkp9bDGDd1w&t=150) [MIDIbox](http://www.ucapps.de/) 与这个项目基于相同的微控制器，所以这绝对是一种可能性。

请查看下面的特雷门琴使用视频。

[https://www.youtube.com/embed/K6bF3Q_YM68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K6bF3Q_YM68?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)