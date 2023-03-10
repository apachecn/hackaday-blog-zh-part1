# 回收的猫喂食器

> 原文：<https://hackaday.com/2010/01/31/recycled-cat-feeder/>

我发现我做了很多有趣的项目，但是当我完成的时候，我不擅长记录它们。假期是用来锻炼的(在我看来)，所以我通常会提前计划，在休息时间做一些很酷的事情。这个项目，我喜欢称之为 Autodine-2009，是感恩节期间的一个自发事件，我正准备写下来。

我们的猫想在早上 6 点被喂食，而且非常坚持。像大多数人一样，我宁愿在一天的那个时候睡觉，所以我做了一个自动喂猫器。现在我们睡觉，而猫在吃东西。我们不想在外出时依靠黑客来喂养我们的猫，所以我没有走[的路线，即一种能够上网的多剂量喂食器](http://hackaday.com/2009/12/03/internet-enabled-cat-feeder/)。相反，我用手头的零件制作了一个带计时器的一次性饮水机。一个伺服旋转一个假底来重力喂猫食。伺服没有控制电路，所以它是由 AVR ATmega8 微控制器通过 h 桥(我不得不为此购买 2 个晶体管)控制的。有两个废弃的触摸开关来设置时间和计时器，还有一个我已经坐了好几年的串行 LCD 显示器。电力来自一个朋友刚刚给我的旧手机充电器，当我问自己“嗯，我可以用它来做什么”时，这个想法产生了。

休息过后，我将通过视频向你们展示这个可回收的装置。这不像我的 AVR 俄罗斯方块版本那么硬核，但我现在更开心了，因为我可以多睡一会儿。

[https://www.youtube.com/embed/ZSnY4T1OP-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZSnY4T1OP-E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)