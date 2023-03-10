# 适合儿童的 RFID 媒体中心播放列表控件

> 原文：<https://hackaday.com/2012/03/15/kid-friendly-rfid-media-center-playlist-control/>

![rfid-dreambox-control](img/8d4d680b4e4284c053336beff3e36e29.png "rfid-dreambox-control")

虽然小孩子拥有大多数黑客/修补匠希望他们不时拥有的小手和手指，但当涉及到操作复杂的电子设备时，他们的精细运动技能并不总是符合标准。人们总是在寻找让他们的孩子也能使用他们的家庭娱乐系统的方法，[，[Humpadilly]也不例外。](http://www.humpadilly.com/?p=93)很像我们本周看到的一些[其他黑客](http://hackaday.com/2012/03/14/rfid-jukebox-for-the-kids/)，他设计了一种方法，让他的小家伙(1 岁和 2 岁)使用 RFID 控制他的 Dreambox 媒体播放器，这似乎是这类事情的首选技术。

除了媒体播放器本身，他的 RFID 遥控器还包括三个主要组件。一台 Arduino 运行该节目，并连接到一个以太网屏蔽和一个装有 ID-20 RFID 阅读器模块的分线板。以太网屏蔽允许 Arduino 通过 telnet 连接与他的 Dreambox 通话，而 RFID 阅读器则做你所期望的事情。

该设备目前还处于起步阶段，虽然[Humpadilly]还没有公布他用来控制系统的实际 RFID 设备的大量细节，但他说更多的细节和改进即将到来。同时，你可以在这里查看他的代码。