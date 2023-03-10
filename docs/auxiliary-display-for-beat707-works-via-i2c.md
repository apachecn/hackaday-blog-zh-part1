# Beat707 的辅助显示器通过 I2C 工作

> 原文：<https://hackaday.com/2011/07/26/auxiliary-display-for-beat707-works-via-i2c/>

![](img/2cbe4fa04879edbd505f630ef56253bd.png "beat707-bigtime")

[Bigtime](https://github.com/Beat707/Beat707-BigTime) 是为[beat 707 MIDI 控制器](http://hackaday.com/2011/04/22/beat707-takes-its-cue-from-a-vintage-drum-machine/)创建辅助显示的简单方法。显示屏的右半部分显示鼓机正在使用的节拍模式，而左半部分记录当前小节。

额外的硬件中只有几个组件。一个四位七段显示器从 ATtiny85 接收数据。由于该微控制器只有 8 个引脚，595 移位寄存器和 CD4067 负责将串行数据转换为点亮显示器所需的输出。整个系统连接到 Beat707 的 I2C 总线，这意味着你不需要对原始系统进行硬件改造，这为更多插件留下了足够的空间。

代码包包括一个 Fritzing 文件，但是为了方便起见，我们在中断后嵌入了一个硬件连接的 PNG。你还可以找到演示视频，其中[古伊列梅]解释了这是如何工作的。

[![](img/e1b98887380845a314b6ed35ea91989d.png "Beat707_BigTime_bb")](http://hackaday.com/wp-content/uploads/2011/07/beat707_bigtime_bb.png)

[https://www.youtube.com/embed/xhpI_UP6tjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xhpI_UP6tjY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)