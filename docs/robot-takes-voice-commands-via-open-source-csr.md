# 机器人通过开源 CSR 接受语音命令

> 原文：<https://hackaday.com/2012/01/12/robot-takes-voice-commands-via-open-source-csr/>

![](img/772d04c361241deb6e85b7d3db7af108.png "speech-recognition-robot")

这是 Chippu，一个[Achu]已经研究了一段时间的机器人。他最近增加的功能是[赋予机器人响应语音命令的能力](http://achuwilson.wordpress.com/2012/01/11/chippu-speech-recognition/)。这是通过使用一个叫做 [Julius](http://julius.sourceforge.jp) 的开源连续语音识别包的变体来实现的。

该软件包依赖于两个主要部分，一组声学模型，让它匹配传入的声音，以及一个参考语法库，它是根据这些声音建立的。[Achu]发表了另一篇文章，详细介绍了在 Linux 平台上使用 Julius 的细节。如果您缩小需要匹配的声学和语法模型的数量，这似乎可以用不太健壮的硬件(例如:在嵌入式系统上)来实现。

目前，Chippu 正在从运行 CSR 的计算机获取命令。但这只是作为一个概念验证,[Achu]计划将机器人过渡到更小的硬件，如 BeagleBoard。

休息之后，请查看视频中 Chippu 响应语音命令的演示。

[https://www.youtube.com/embed/WHMeLI0H9f4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/WHMeLI0H9f4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)