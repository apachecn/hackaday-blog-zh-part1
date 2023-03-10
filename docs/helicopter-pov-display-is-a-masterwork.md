# 直升机视角显示是一个杰作

> 原文：<https://hackaday.com/2010/11/12/helicopter-pov-display-is-a-masterwork/>

![helicopter hack LED mod](img/235d998ac75fd6c522cb797992a34b55.png "helicopter-pov")

是啊！带有相当高分辨率视觉暂留显示的无线电控制直升机是一件漂亮的东西。[Mziwisky]的作品是沿着原型法的几个步骤[的结果。他在试验板上建立了一个 POV 测试平台，为这个项目设计了他的第一个 PCB，然后开始构建它。在最初受到](http://mziwisky.wordpress.com/category/helipov/)[一个 POV 吊扇](http://hackaday.com/2009/07/22/ceiling-fan-pov/)的启发后，【Mziwisky】环顾四周，看看是否还有其他人已经在直升机上安装了显示器。事实上，[这在](http://www.nightgraphix.de/)之前就已经完成了，但是关于构建的细节很少。

直升机有两个桨叶，每个桨叶上都有相同的硬件，每个桨叶都耗费了大约 10 个小时的组装时间。他基本上建立了一个印刷电路板，使用刀片作为基板，通过粘贴粘合铜箔。这构成了 led 的矩阵，并连接到一个小电路板，该电路板带有一个 ATmega8 和一些安装在刀片内侧的移位寄存器。还有一个 180 毫安的 LiPo 电池组，和一个霍尔效应传感器来同步每个显示器。结果是惊人的，正如你在休息后的视频中看到的那样，但为了完全驯服每个转子上的 32 个 led，还有一些问题需要解决。

有点像[未来正在发生](http://hackaday.com/2009/08/24/autogiro-pov-nostalgia/)。

[https://www.youtube.com/embed/LKTC1lmXnpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/LKTC1lmXnpc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)