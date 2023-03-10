# 唱机的 MIDI 输入

> 原文：<https://hackaday.com/2011/02/04/midi-input-for-the-kaossilator/>

![](img/f2d97138edddcd21ff4a3b0f727bbdbe.png "kaossilator-touchpad-hack")

这不是严格的 MIDI 输入黑客；[furtek]为他目前使用的 MIDI 连接的 Kaossilator 完成了另一个输入破解。在它未被敲击的形式中， [Kaossilator](http://www.korg.com/kaossilator) 是一个基于触摸板的小型声音操作工具。[furtek]发现了如何在这个小设备上读取和使用触摸板数据。然后他设计了一个 ATtiny2313 作为电路的核心来欺骗这些信号。微控制器现在监听输入的 MIDI 数据，在一个表中查找适当的信号转换，然后将它们输出到 Kaossilator。

在休息后的视频中，你可以看到它完美地工作，没有滞后或明显的问题。正如我们在上面提到的，可以做得更多。由于 ATtiny2313 只是将 MIDI 转换成触摸板信号，因此输入可以是任何东西。我首先想到的是一个舞池，它可以根据有多少人在跳舞来改变音乐。

[https://www.youtube.com/embed/Jmzb8iC33RA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Jmzb8iC33RA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)