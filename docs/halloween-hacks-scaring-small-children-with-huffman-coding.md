# 万圣节黑客:用霍夫曼编码吓唬小孩子

> 原文：<https://hackaday.com/2011/10/19/halloween-hacks-scaring-small-children-with-huffman-coding/>

![](img/51f7563505680f7a216a5ccb8ac25384.png "Halloween")

![](img/1dc4d3c60078730e55c58c057f4debbc.png "Minolta DSC")

NerdKits 的团队决定为万圣节做点什么。只有在万圣节吓唬小孩子是一个令人钦佩的目标，所以他们演示了一种在门被打开后播放令人毛骨悚然的声音的方法。

为了触发声音，一个来自警报系统的磁簧开关被连接到前门。这触发了微控制器，稍有延迟，一些令人毛骨悚然的音频就可以在一对扬声器上播放。该团队决定将所有音频数据存储在他们的 ATmega328p 的闪存中，但这不允许发出很长的尖叫声。为了延长被诅咒者的哭泣声，NerdKits 团队决定使用[霍夫曼编码音频](http://en.wikipedia.org/wiki/Huffman_coding)。

因为 Huffman 编码依赖于最常见的值被分配最短的代码，所以团队使用了一点 Python 和 C magic 来为他们的音频文件找出最佳编码。在邪恶的笑声被充分压缩后，微控制器被编程来解码音频并将其发送到一对扬声器。该团队为他们的项目准备了所有的软件，在这里供你阅读。

虽然这个项目可以用一个 Arduino 和一个 MP3 盾在一个小时内完成，但 NerdKits 团队希望让孩子们学习*事物如何工作，这也是一个令人钦佩的目标。来自 NerdKits 的[Humberto]放了一个视频来解释这个项目的理论。休息之后来看看。*

[https://www.youtube.com/embed/mE-kCSjbauw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mE-kCSjbauw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)