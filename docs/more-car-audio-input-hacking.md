# 更多汽车音频输入黑客

> 原文：<https://hackaday.com/2010/08/15/more-car-audio-input-hacking/>

![](img/7d17ca4031528210610f003a9f56fc56.png "dash-cassette-to-ipod-input")

[Dave]从他的仪表板中拉出主机，添加一个 iPod 输入。他采取了比我们几天前看到的的另一个黑客[更具侵略性的路线。他实际上接入了从杜比阅读器芯片到放大器的音频线路。](http://hackaday.com/2010/08/12/adding-an-input-to-an-old-head-unit/)

第一步是欺骗卡座认为它有一盒磁带插入。他观察了其中一个芯片上的使能引脚，以发现时序，并使用 PIC 微处理器模拟该信号。他从那里取出读取磁带数据的芯片，直接接入音频输出轨迹。这在给 iPod 充电时出现了一些噪音问题，但[戴夫]用一些去耦电容解决了这个问题。