# 通过 FPGAs 的两个玩家空间入侵者

> 原文：<https://hackaday.com/2012/01/03/two-player-space-invaders-via-fpgas/>

上学期，[Peter]、[Jared]和[Jeremy]选了一门关于嵌入式系统的课程。他们设法在他们班上制作出经典的《太空入侵者》的精确复制品。不想浪费好的代码，他们决定开发[两个玩家太空入侵者](http://www.undiscoveredfeatures.com/2012/01/space-invaders-2-player.html)，我们不介意测试一下。

这些家伙在 Virtex II 开发板上建造了他们的太空入侵者克隆体。想要更多一点的硬件开发，他们拿起一对[射频收发器](http://www.sparkfun.com/products/9582)，这样两块电路板就可以相互通信。双人太空入侵者的规则相当简单；如果你消灭一个外星人，有 30%的几率它会出现在你对手的屏幕上。击中沿屏幕上方飞行的宇宙飞船，对手屏幕上会出现 1 到 7 个外星人。这有点像双人俄罗斯方块，你的胜利带来了你朋友的垮台。

这些家伙在一个旧游戏上做了一个非常漂亮的旋转，我们很想尝试一下。休息过后，看看左边的家伙输给了他的实验搭档。

[https://player.vimeo.com/video/34487751](https://player.vimeo.com/video/34487751)