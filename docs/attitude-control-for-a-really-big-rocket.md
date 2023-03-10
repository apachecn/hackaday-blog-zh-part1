# 大型火箭的姿态控制

> 原文：<https://hackaday.com/2011/01/18/attitude-control-for-a-really-big-rocket/>

![](img/ec2c24affbd9094306c3eac719bf21fe.png "rocket-attitude-control")

如果这是模型火箭，那它一定是我们见过的最大的。[斯科特]和[特雷弗]在阅读了一些关于这个主题的研究后，承担了[建造火箭姿态控制系统](http://scott-n.com/wp/?p=20)的任务。但是研究人员只是用模拟来测试这些理论，所以他们开始建立自己的理论。上面的原型有一个压缩氮气罐，可以容纳高达 3000 磅/平方英寸。你就可以开始理解为什么这个需要用大火箭了。加压气体通过一个调节器与四个阀门相连，这些阀门向机身周围的喷嘴供气。Arduino 从陀螺仪获取读数，并通过继电器板驱动气阀。

休息过后，你可以看看视频中的试验台。原型水平悬挂在电线上，其方向由系统保持在一个位置。如果你对进入稳定控制的方程式感兴趣，还有一篇论文。这个系统应该就在我们 10 月份看到的[号巨型糖火箭](http://hackaday.com/2010/10/03/hackaday-links-october-3-2010/)上。

[https://www.youtube.com/embed/Mqttm0ay8gk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mqttm0ay8gk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)