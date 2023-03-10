# 从重复使用的零件中避开六足障碍

> 原文：<https://hackaday.com/2011/07/19/obstacle-avoiding-hexapod-from-reused-parts/>

![](img/230ffba7502e00b5676653e1bee63778.png "dorkboard-hexapod")

一天，当他下班后有空的时候，他建造了这个六足机器人。就像[我们看到的最后一个六足机器人](http://hackaday.com/2011/07/11/crafting-a-hexapod-with-an-rc-controller/)一样，他基于[的 Pololu 设计](http://hackaday.com/2010/01/18/the-polulu-3-servo-hexapod/)构建，该设计使用三个伺服电机来实现令人惊讶的可靠运动。

硬件非常简单。一个书呆子板充当大脑。它是一个 PCB，每边都比标准 AVR 28 引脚微控制器宽一个母引脚。这使得 Arduino 芯片上的所有引脚都很容易接近，同时使其变得小巧轻便。你可以看到一个四组电池挂在伺服电机下面提供动力。

突出在六腿支架上方的是[一个超声波测距仪](http://www.parallax.com/tabid/768/ProductID/92/Default.aspx)。这为小机器人增加了自主性，休息后你可以在视频中看到它运行一些避障例程。我们已经问过[Rob]是否可以分享他的代码，如果我们收到他的回复，我们会更新这篇文章。

**更新:**这里是[到草图](http://dl.dropbox.com/u/32611590/Arduino/Sketches/hexapodv1.pde)的链接，我们用【Rob】发给我们的一张图片更新了这张图片。

[https://www.youtube.com/embed/j2glaziGW5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/j2glaziGW5g?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)