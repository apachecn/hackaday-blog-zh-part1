# 制作新办公室时钟的原型

> 原文：<https://hackaday.com/2011/06/01/prototyping-the-new-office-clock/>

![](img/e00596145953ecf96ba2e07d6237f9d1.png "arduino-xbee-clock-pair")

[损坏]被点击来建立一个新的时钟挂在办公室的墙上。他得到了一些用于小时和分钟的 6.5 英寸七段显示器，以及一些用于日期和月份的 4.5 英寸模块。他没有直接使用大型硬件(特别是因为他在等待 PCB 订单的到来)[而是用更普通尺寸的显示器建造了这个原型](http://damage.hackhut.com/2011/05/28/arduino-based-large-digital-clock-with-7-segment-display/)。

他的建筑由 Arduino 驱动。在休息后的视频中，他提到了保持时间的温度补偿晶体振荡器。我们打赌这就是 Sparkfun 出售的基于 DS3234 的 RTC 模块[。这是与](http://www.sparkfun.com/products/10160) [Chronodot](http://hackaday.com/2009/10/27/parts-chronodot-rtc-module-ds3231/) 相同的芯片家族，它是我们为[乒乓时钟](http://hackaday.com/2011/01/31/how-to-build-a-ping-pong-ball-display/)选择的。

完成后的时钟会高高挂在墙上，当你需要设置时间时，就够不着了。这应该不需要做太多——如果有的话——因为 RTC 包括一个备用电池。但是[损害]还是花时间开发了一个远程编程设备。他使用另一个 Arduino、一个 LCD 显示器和一对 Xbee 迅速制作了一个遥控器，可以用来导航和改变主机的设置。

[https://www.youtube.com/embed/Qql_7a3p8tk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Qql_7a3p8tk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢保罗]