# 自平衡机器人保持直线和狭窄的东西

> 原文：<https://hackaday.com/2011/03/03/self-balancing-robot-keeps-things-on-the-straight-and-narrow/>

![self_balancing_robot](img/6d452e84c519e8da36fe449087089062.png "self_balancing_robot")

[James]在 MatLab 中设计了一个数字控制器，但他真的想看看它是否能在现实应用中工作。为了测试他的线性二次调节器设计，他决定制造一个自平衡机器人。他的目标是[建造一个即使受到外力也能保持平衡的机器人](http://letsmakerobots.com/node/25532),同时保持在同一位置。

在一对轮子上保持平衡并不那么简单，所以他的 LQR 控制器允许他权衡机器人保持平衡的优先事项，一旦达到平衡，就专注于返回到它的起始位置。正如你在下面的视频中看到的，结果令人印象深刻。一旦接通电源，机器人就能很容易地达到平衡，即使在被推动或物体放在它上面时，它保持稳定也没有问题。

[James]计划在不久的将来进行几项增强，包括通过 Xbee 模块进行远程控制，以及利用声纳或可能的摄像头进行自主导航。我们非常希望在未来的版本中看到它配备 Kinect 传感器，但这只是我们的想法！

请继续阅读他整理的几个演示视频。

[谢谢，尼古拉斯]

[https://www.youtube.com/embed/aEA_z30OAIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aEA_z30OAIY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[https://www.youtube.com/embed/aTBhkkZyKgc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aTBhkkZyKgc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)