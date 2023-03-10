# 相量 A/V PAL 演示使用 ATmega88

> 原文：<https://hackaday.com/2010/05/01/phasor-av-pal-demo-uses-atmega88/>

[https://www.youtube.com/embed/sCN1bqRG-7o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sCN1bqRG-7o?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

上面是一个由[Lft]开发的名为 Phasor 的新演示视频。它由 AVR ATmega88 和一些无源元件运行，结果相当惊人。[Lft] [详细介绍了他使用的技巧](http://www.linusakesson.net/scene/phasor/index.php)来启动和运行这个系统。该芯片的时钟频率为 17.73447 MHz，正好是 PAL 彩色载波频率的四倍，这使得他可以伪造一个平滑的信号。他还使用一个定时器来获得他需要的电压。这里所做的工作超出了硬核范围，坦率地说，我们无法相信他设法将所有这些都放入 8.5 KB 的程序空间，而只有 1 KB 或 ram。我们想知道那里是否有足够的空间给 AVR 俄罗斯方块项目的[添加声音和色彩。](http://hackaday.com/2010/01/18/more-avr-tetris/)

[感谢雪碧 _tm]