# 关于 PS3 六轴控制器 USB 通信的所有信息

> 原文：<https://hackaday.com/2011/03/11/all-about-ps3-sixaxis-controller-usb-communications/>

![](img/b78cfefbaac3172681be89ab63b4c26b.png "sixaxis-usb-communications")

[Austyn]目前正在对 PlayStation 3 六轴控制器的 USB 通信进行逆向工程。你可能会想这已经完成了，但是[Austyn]找不到有用的源代码，所以他开始了自己的项目 libopenaxis。

他用来嗅出 USB 通信的过程很有趣。他利用 GlovePIE 来获取控制器的 USB 请求块。手里拿着 DIY Kinect 黑客教程中使用的 Python 脚本[开始转储控制器数据。每按一次键，脚本就会读出完整的数据包，用来计算数据结构是如何组织的。](http://www.ladyada.net/learn/diykinect/)

这个项目已经知道了所有的数据类型，但是现在大多数变量的用途还是未知的。希望随着时间的推移，这些空白会被填补。有两件事是肯定的；如果你对编写可以与 PS3 控制器通信的 Python 代码感兴趣，这是一个很好的信息来源，过去几个月观看 Kinect hacking 非常有趣，现在仍在开花结果。