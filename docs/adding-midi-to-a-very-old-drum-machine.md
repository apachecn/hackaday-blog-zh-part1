# 将 MIDI 添加到非常旧的架子鼓上

> 原文：<https://hackaday.com/2011/05/13/adding-midi-to-a-very-old-drum-machine/>

![](img/c69da3e67a8ea8ffacd41e59186f1692.png "cr68")

在架子鼓演奏来自 SD 卡或 EPROM 的样本之前很久，鼓的声音是模拟的——只是经过过滤的波形和噪音。在现代人看来，这些是非常原始的机器，但对[安德鲁]来说，它们是这个[杰出黑客](http://www.andrewkilpatrick.org/?p=cr68_midi_input)的灵感来源。

[Andrew]拿了一台 1978 年的 Roland CR-68 鼓机，在 PIC 微控制器的帮助下增加了 MIDI 输入。由于不想改变机器的外观，[Andrew]对 PIC 进行了编程，以便在设备通电时观察启动/停止按钮。如果按钮被按住，PIC 进入它的编程模式，来自 CR-68 的声音可以被映射到 MIDI 控制器上的单个音符。没有提到 PIC 是否查询中的触发器来修改预设模式的速度，但我们假设这将是一个相对简单的实现。尽管如此，对于一台比 MIDI 早 4 年制造的机器来说，还是非常令人印象深刻的。

我们喜欢[Andrew]的作品，我们也为任何未来的拥有者感到高兴，他记录了如何使用他的设备(并巧妙地将其贴在鼓机的底部)。很高兴看到旧鼓机在样本被记录后，不仅仅被用于门挡。休息之后，请观看[Andrew]的走过视频。

 [https://www.youtube.com/embed/pwjvmjWjtSY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/pwjvmjWjtSY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)