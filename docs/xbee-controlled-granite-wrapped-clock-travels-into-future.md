# Xbee 控制，花岗岩包裹的时钟旅行到未来

> 原文：<https://hackaday.com/2011/01/27/xbee-controlled-granite-wrapped-clock-travels-into-future/>

![](img/9c8585f4015ab4b9104e3ee91385211b.png "xbee-controlled-clock")

从表面上看，这个钟比它的时间快了几个月。[Oscar] [建造了时钟](http://blog.bricogeek.com/noticias/tutoriales/bricoclock-reloj-gigante-casero-con-arduino/) ( [翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=auto&tl=en&u=http://blog.bricogeek.com/noticias/tutoriales/bricoclock-reloj-gigante-casero-con-arduino/))花时间将许多好东西添加到组合中。首先，你看到的部件包括六个大的 7 段显示屏，分别显示小时、分钟和秒，以及一个可以滚动消息的 LED 字幕。内部有一个用于环境反馈的温度和湿度传感器，以及一个允许无线计算机控制的 Xbee 模块。时间由一个 [DS1307 实时时钟](http://hackaday.com/2010/07/26/ds1307-breakout-board/)保持，该时钟由一个 Arduino Uno 读取，然后由一对 I2C 可寻址 SAA1064 驱动器推送到显示器。整个盒子被四块花岗岩包裹着，前面是一块玻璃。我们当然希望它能牢牢地固定在墙上。休息之后你可以看到它在滴答滴答地走着。

[https://www.youtube.com/embed/lAV3yu9RDlM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lAV3yu9RDlM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)