# 现场直播的 NBA 记分牌，带有巨大的 7 段显示屏

> 原文：<https://hackaday.com/2011/07/28/live-nba-scoreboard-with-huge-7-segment-displays/>

[![](img/d33111e2227dba7008ad30dde4a76469.png "board")](http://hackaday.com/wp-content/uploads/2011/07/board.png)

[Kianoosh]春假期间在拉斯维加斯，被赌场显示的实时体育比分迷住了。他认为这是一个很容易复制的项目，所以他建造了一个巨大的 NBA 记分牌，可以从 NBA 网站上实时更新。

该版本使用 OS X 自动机从 NBA 的移动网站上下载分数。通过用 Java 编写的解析器发送，然后分数通过 XBee 发送到 ATMega32。[Kianoosh]贴出了所有的代码和原理图，以及一份 [PDF 书面报告](http://kiantech.me/storage/files/LiveNBAsm.pdf)。因为记分牌与运动无关，[Kianoosh]计划为 NFL、MLB 和 NHL 编写新代码。我们对这种构造印象深刻，加上[巨型 7 段 led](http://www.elexp.com/opt_0165.htm)，这将是一个体育酒吧(或真的*任何*酒吧)的绝佳补充。

[Kianoosh]录制了一段他的记分牌的视频(从 2011 年 4 月 13 日开始，如果你想知道的话)。下面来看看吧。

[https://www.youtube.com/embed/M5VDC8qn8Gc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M5VDC8qn8Gc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)