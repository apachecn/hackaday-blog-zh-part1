# 在微控制器上下棋

> 原文：<https://hackaday.com/2011/07/06/playing-chess-on-a-microcontroller/>

![](img/80961fd46998d5be8d9a22e53dec2e95.png "Chess")

[Arthur Benemann]为他的电子工程项目开始了一个小项目，并遭受了我们所见过的最糟糕的功能蠕变情况。他刚刚发布了他的 [picChess](http://www.instructables.com/id/picChess/) 项目的一个指令，可以在 VGA 显示器上下棋，带有键盘、声音、时钟和温度传感器。显然，有一天晚上[亚瑟]无聊了，扔进了一个康威的生活游戏的实现。

[Arthur]为他的项目选择了一款 DSPIC33F μC，所有东西都放在面包板上。他对自己的 VGA 程序相当自豪，这是他第一次使用 DMA。我们对[Arthur]的象棋引擎印象深刻——这是我们在 Hack A Day 上看到的第一个自制象棋引擎。虽然这个引擎是一个蛮力搜索，带有阿尔法-贝塔修剪，引擎本身看起来相当先进，甚至支持 T2 阉割。

虽然不支持 [a](http://en.wikipedia.org/wiki/Threefold_repetition) [少数](http://en.wikipedia.org/wiki/Fifty-move_rule) [规则](http://en.wikipedia.org/wiki/En_passant)并且不知道引擎的 ELO 评级，但是【亚瑟】的引擎应该还是能打败一个业余玩家的。的确是一个令人印象深刻的壮举。

休息之后看看[亚瑟]的视频。

[https://www.youtube.com/embed/G27dC_rapko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/G27dC_rapko?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)