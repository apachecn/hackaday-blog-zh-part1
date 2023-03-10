# 逆向工程 MyKeepon

> 原文：<https://hackaday.com/2011/11/09/reverse-engineering-mykeepon/>

[qDot]最近得到了一个 MyKeepon 玩具，在摆弄了一会儿后，他决定把它拆开来看看里面有什么。他希望轻松地改造这个玩具，但就像大多数黑客冒险一样，事情可能比他最初想象的要花更长的时间。

在他的拆卸过程中，你可以看到组成 MyKeepon 的各种组件，包括三个移动电机，以及一系列按钮和一个用于与玩具互动的麦克风。当然，他最感兴趣的部分是我的 Keepon 的电路板，因为那是真正的工作开始的地方。

在那里，他发现了两个主处理器 Padauk 处理器芯片，在其数据手册中被描述为“现场可编程处理器阵列”。他说，该品牌是众所周知的从 PIC 数据表中一字不差地提取文本，所以他对那里打印的内容没有太大的信心。撇开粗略的文档不谈，他在连接两个芯片的 I2C 总线上四处打探，能够嗅到一点流量。他正在记录他的发现，你可以在他的 Github 项目网站上看到更多。

他已经对玩具做了一些简单的修改，但是在他完全控制它之前还有很多事情要做。他的工作肯定会让无数 MyKeepon 粉丝开心，包括我们自己的[Caleb Kraft]，他对这个玩具的喜爱可以从下面去年 CES 上拍摄的视频中看出。

[https://www.youtube.com/embed/yQhMtuYZj4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yQhMtuYZj4Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)