# 下水道堵塞警报系统

> 原文：<https://hackaday.com/2009/07/27/sewer-clog-alert-system/>

![xbee](img/824608161a36a17ed3aebcfe3e653884.png "xbee")

[miketysklar]注意到当地一家企业的污水管道有问题。人们不停地把卫生棉条冲进厕所，结果堵塞了水泵。他们已经安装了一组灯和喇叭，以便在堵塞时熄灭，但他们希望有短信功能，这样他们就能知道自己在哪里。新系统通过[在闪光灯激活时给 XBee](http://www.flickr.com/photos/11461247@N02/3762972121/) 供电来控制闪光灯。它发出的信号被另一个 XBee 接收，该 XBee 连接到运行 [python 脚本](http://www.flickr.com/photos/11461247@N02/3763022607/)的计算机上。该脚本然后通过电子邮件发送短信给这个可怜的家伙，由他来解决这个问题。

相关:[无线引导加载](http://hackaday.com/2009/01/28/wireless-bootloading/)