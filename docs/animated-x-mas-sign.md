# 动画 X-mas 符号

> 原文：<https://hackaday.com/2011/10/10/animated-x-mas-sign/>

![](img/12379eff054b7a88bf9be3a751bca65e.png "Christmas")

当然，离圣诞节可能还有两个半月。这并不意味着我们不能开始制作一些圣诞装饰品。去年，嵌入式实验室的[RB]使用简单的微控制器设置制作了一个[动画圣诞标志](http://embedded-lab.com/blog/?p=1260)。今年，[RB]增加了一个闪烁的 LED 边框，并用 74xx ICs 完成了整个项目。

今年标志的字母是从去年的字母中回收的。然而，这一次，两串 12 个 led 被用于闪烁的边框。闪烁电路使用 74hc14 施密特触发器来提供时钟。一对 74hc595 移位寄存器一次打开一个字母。速度由一个小的微调电位器控制。

使用集成电路来驱动一系列图案中的灯并不是一件新鲜事——你很难在六七十年代的科幻电影中找到类似的设置。当然这个标志不能和一个 [~~微处理器~~很多耐心](http://www.youtube.com/watch?v=rmgf60CI_ks)所能做的相比，它仍然是一个非常好的构建。休息之后，请观看视频，了解 X-mas 标志的运行情况。

[https://www.youtube.com/embed/KPSQhY1g5dE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KPSQhY1g5dE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)