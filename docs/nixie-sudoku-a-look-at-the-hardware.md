# 谢妮数独:看硬件

> 原文：<https://hackaday.com/2010/07/19/nixie-sudoku-a-look-at-the-hardware/>

![](img/e65ef17930f86d91a140fb2bd906de89.png "nixie-sudoku-hardware")

我们总是很高兴能参观一下让事情运转的勇气。[约翰·萨里克]贴出了几张照片和对硬件的描述，这些硬件组成了他的[谢妮数独游戏](http://hackaday.com/2010/07/09/nixie-sudoku/)。模块化设计使用专业制造的电路板，极大地提高了此类大型电路的耐用性。

该设计借鉴了类似硬件的好创意。Ogi Lumen 的谢妮 Duo 套件允许将灯管安装在带有级联移位寄存器的驱动板顶部，以控制多达 8 根灯管。 [ArduiNIX 屏蔽](http://hackaday.com/2009/11/02/arduinix-nixie-shield-for-arduino/)使得 Nixies 所需的高电压很容易用 Arduino 控制。不，[约翰]不仅订购了这些套件，还将它们相互插接。他设计了自己的板子来满足自己的需求。每个驱动板可以控制一个 3×3 网格中的 9 个电子管，全部在一个 PCB 上。他的高压板可以为整个系统提供足够的电力，整个系统由一个 Arduino 板连接在一起。

他的文章很有趣，所以你一定要看一看。他还拍摄了一段视频，我们在休息后嵌入了这段视频。它澄清了一些问题，例如显示使用闪烁的小数点来指示当前光标位置。

[https://www.youtube.com/embed/YoixTdJzMoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YoixTdJzMoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)