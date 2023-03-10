# 增加数字伺服电机的运动范围

> 原文：<https://hackaday.com/2012/03/14/increasing-a-digital-servo-motors-range-of-motion/>

![](img/46fd2f7d3a87ea8853189d8fe22386dc.png "increasing-servo-range-of-motion")

不满意这个数字伺服电机 120 度的运动范围[Malte]开始扩大其灵活性。他找到了一个办法，[改变反馈电位计，以便给电机一个更宽的范围](http://www.mtahlers.de/index.php/diverses/servohacking-ii) ( [翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwww.mtahlers.de%2Findex.php%2Fdiverses%2Fservohacking-ii))。

测试视频(插播后嵌入)显示了他修改前后的刻度线。你可以看到更宽的刻度线更接近他感兴趣的 180 度范围。控制方法与以前没有什么不同，内部电路仍在监听脉冲在 1 到 2 毫秒之间的控制信号，以确定伺服喇叭的位置。[Malte]在反馈电位计的两个外侧引脚上增加了电阻。这是控制电路为了判断伺服喇叭的位置而测量的。他在演示中使用了 1.6k 欧姆的电阻。但他不是随便扔进去的。他的文章讨论了他用来确定他想要的电机位置的目标电压的计算。

[https://www.youtube.com/embed/YjQjU343sTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/YjQjU343sTE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)