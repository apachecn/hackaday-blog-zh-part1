# DIY 赛格威回收坏掉的电动滑板车

> 原文：<https://hackaday.com/2011/07/25/diy-segway-recycles-broken-electric-scooters/>

[![](img/be92284e24c9b4bf7121d709725b10ff.png "segway")](http://hackaday.com/wp-content/uploads/2011/07/segway.jpg)

[Petter]用几辆便宜的电动滑板车为自己做了一辆 DIY Segway。我们在过去已经看到了几个非常好的赛格威版本，如[全模拟赛格威](http://hackaday.com/2010/12/10/segfault-balancing-transport-using-a-dozen-op-amps/)，或[令人毛骨悚然的行走版本](http://hackaday.com/2010/11/26/dodecapod-to-offset-segway-as-futuristic-transport/)，【彼得】的赛格威版本看起来像是一个有用的人类运输设备。

马达、链条、齿轮和轮子都是从一对电动滑板车上拆下来的。左右转向是通过左右倾斜车把来实现的。车把本身在一个[底座](http://p1r.crf.nu/files/2011/07/joint.png)处连接到关节上，允许它们被拿上和拿下。我们认为这对于把一辆[彼得]的赛格威扔进汽车后备箱来说很棒——这是最初的赛格威所没有的设计特征。

该项目的电子设备基于 ATMega168，它从加速度计和陀螺仪读取数据。电机由两个 H 桥控制，由两个串联的 12 V 铅蓄电池供电。我们不确定这种电池在现实世界中能坚持多久，但[彼得]的制造速度似乎足够快。

查看下面的演示视频:

[https://www.youtube.com/embed/MBOQ6RMk6aw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MBOQ6RMk6aw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)