# 数字坐标探测器

> 原文：<https://hackaday.com/2011/07/25/digital-cootie-detector/>

[![](img/900a8f399bc5a2a036f1db434ffc95d5.png "cootie")](http://hackaday.com/wp-content/uploads/2011/07/cootie.png)

孩子们喜欢排斥游戏。这通常表现在“远离”、“让某人去抓虱子”或一直流行的“没有布莱恩俱乐部”等游戏中。[Rob]写信告诉我们他建造的数字虱子探测器。cootie 探测器根据皮肤电反应工作。它实际上非常类似于一个 [E-Meter](http://www.cs.cmu.edu/~dst/E-Meter/) ，尽管这个设备测量的不是 tans 而是实际存在的东西。

[皮肤电反应](http://en.wikipedia.org/wiki/Skin_conductance)是对皮肤导电性的测量。皮肤的导电性会发生变化，因为当有人紧张时，汗腺会被激活。这是一种心理唤醒的措施，使其成为排斥游戏的伟大探测器——不想要虱子的孩子会“让自己紧张起来”,给自己虱子。

该构建基于 ATtiny45，仅需要几个电阻和回形针即可完成一个完整的构建。“Cootie 检测算法”以闪光灯开始，这是一种让某人紧张的好方法。测试完成后，绿灯表示他们可以进入隔离区，红灯表示他们必须被排除在外。还有一种“设备被篡改”的结果——红灯和绿灯交替——当一个聪明的孩子试图短路回形针引线时就会显示出来。查看下面的演示:

[https://www.youtube.com/embed/xgkBPqhUnNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xgkBPqhUnNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)