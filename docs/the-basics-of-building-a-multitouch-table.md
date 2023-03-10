# 构建多点触控桌子的基础

> 原文：<https://hackaday.com/2011/04/16/the-basics-of-building-a-multitouch-table/>

这里是一个简单的多点触控桌面设置。几年前，当塞思·桑德勒完成[mt mini build](http://hackaday.com/2008/05/20/multitouch-project-roundup/)时，我们看过他的多点触控作品。他把 MTbiggie 的尺寸放大了一点，向你展示了组装起来是多么容易。上面看到的演示装置只是几把椅子、一张丙烯酸板、一面镜子、一台投影仪、一台电脑和一个 diy 红外网络摄像头。

当你的手指接触丙烯酸表面时，这个装置使用周围的红外光来检测手指的轮廓。一个带有曝光胶片过滤器的网络摄像头将表面下接收到的红外光图像传送给计算机。传入的视频使用[社区核心视觉](http://sethsandler.com/multitouch/community-core-vision-guide/)进行处理，其中每个单独的点都被隔离和映射。一旦有了数据，你的发展前途无量。[Seth 的]演示包包括一个鼠标驱动程序，一些物理应用程序，一个愤怒的小鸟实现，和一些其他的。休息后在视频里自己看吧。

[https://www.youtube.com/embed/sJU8sBt7eC8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sJU8sBt7eC8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)