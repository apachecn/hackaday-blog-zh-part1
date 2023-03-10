# 用电视遥控器玩蛇

> 原文：<https://hackaday.com/2011/09/06/playing-snake-with-a-tv-remote/>

![](img/024841e5c1654ef711191dd3015b7708.png "snake")

[vinod]把他的贪吃蛇游戏和*游戏*的副本发送到老式的诺基亚哑手机上。

该版本基于 PIC16F877 微控制器[，就像我们之前看到的 Snake 版本一样](http://hackaday.com/2010/06/28/links-expanded-snake-on-led-matrix/)，但是【vinod】在他的版本中没有使用物理按钮。相反，他使用飞利浦红外电视遥控器来控制游戏。红外控制器只占用微控制器的一个引脚，而最简单的四按钮设置需要 4 个引脚。[vinod]还提供了一个简单的单晶体管电平转换器，因此 Snake 可以通过 RS-232 在 PC 上播放。PIC 代码包含在构建中，这是一个伟大的构建，提醒我们一个更加文明的时代。

[vinod]玩蛇游戏的视频在休息后发布，但我们注意到蛇可以在 LED 矩阵的两侧“弯曲”。有些人可能会认为这是作弊，但这可以通过修改几行代码来解决。

[https://www.youtube.com/embed/EuEvCTFW_AI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EuEvCTFW_AI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)