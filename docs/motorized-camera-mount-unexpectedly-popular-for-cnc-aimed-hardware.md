# 电动相机安装出乎意料地受数控硬件的欢迎

> 原文：<https://hackaday.com/2011/12/20/motorized-camera-mount-unexpectedly-popular-for-cnc-aimed-hardware/>

![](img/2f396d8e05bf2c9f47f17b371d81dacf.png "motorized-linear-camera-mount")

这是一个[相机支架，它沿着一个机动雪橇](http://www.buildlog.net/blog/2011/12/makerslide-camera-slider-control-program/)平稳移动。[Bart Dring]创建了这个系统，并对它的受欢迎程度感到惊讶，已经收到了来自摄影师的几个销售请求。他[最初设计了直线轴承](http://hackaday.com/2011/05/10/open-source-linear-bearing-system/)系统，称为 MakerSlide，作为其他数控机床解决方案的廉价替代品。当时，他还不知道如何让计算机为视频拍摄绘制定时运动，但正如你在休息后的剪辑中看到的那样，MakerSlide 在这方面做得非常出色。

模块化履带系统便于安装在底座上。在这种情况下，几片丙烯酸树脂让他在标准的相机三脚架上支撑轨道的两端。[Bart]提到在决定如何控制系统时，数控铣削硬件工作人员和摄影师之间的知识差距是一个问题。由于摄影师不太可能精通 EMC2，他用 Arduino 设计了一个控制应用程序。它使用步进电机控制器屏蔽，并做一些奇特的数学运算，以确保有平稳的加速等。

[https://www.youtube.com/embed/xt77g-Zzdjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xt77g-Zzdjs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)