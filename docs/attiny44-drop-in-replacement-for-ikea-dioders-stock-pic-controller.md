# ATtiny44 宜家 Dioder 库存 PIC 控制器的替代产品

> 原文：<https://hackaday.com/2012/03/28/attiny44-drop-in-replacement-for-ikea-dioders-stock-pic-controller/>

![](img/c934d62e69ce225b1c77e5f33095e256.png "dioder-with-drop-in-attiny44")

Ikea Dioder 是一款 LED 灯，在蓝色和黄色相间的大楼里出售，你可以通过简单的按钮和滚轮控制器来调配自己的颜色。[Marco Di Feo]查看了所有其他改变控制器的项目，发现可以用 ATtiny44 微控制器直接替换 IC。随着芯片焊接到电路板上，他增加了红外控制，这样他[就可以用他的通用遥控器](http://marco-difeo.de/2012/03/28/irdioder-ikea-dioder-hack-mit-atmel-und-infrarotempfanger/) ( [翻译](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fmarco-difeo.de%2F2012%2F03%2F28%2Firdioder-ikea-dioder-hack-mit-atmel-und-infrarotempfanger%2F))改变颜色。

[Marco]移除了通常负责选择颜色的电位计。这释放了微控制器上的一个引脚，他可以用它来接收来自 TSOP1736 IR 接收器的信号。休息后的视频显示，该设备照亮了他的家庭娱乐中心的背面，对他的遥控器的命令做出反应。

当然，这可以在没有芯片交换的情况下完成，因为附带的 PIC 16F684 可以就地重新编程。但是[Marco]手头没有 PICkit 或其他程序员。T3[https://www.youtube.com/embed/1tQ_aqayWZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/1tQ_aqayWZk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)