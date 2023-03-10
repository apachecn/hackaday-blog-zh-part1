# 密码保护的激光绊网报警系统

> 原文：<https://hackaday.com/2011/03/11/passcode-protected-laser-tripwire-alarm-system/>

![laser_tripwire](img/ca4f7a9b76e246de160b82953357d4a2.png "laser_tripwire")

有时，安全性不需要过于复杂就能有效。Instructables 用户[1234itouch]最近制造了一个[简单的激光绊网报警器](http://www.instructables.com/id/Arduino-laser-detector-with-keypad/)，它可以安装在几乎任何地方，配有一个键盘用于解除设备。

他在一个项目箱中安装了一个光电池，还有一个 Arduino 和一个 12 键键盘。激光笔从一个缝隙中瞄准光电池，这导致 Arduino 读取稳定的电压。当激光束中断时，会检测到电压下降，警报会响起，直到您输入正确的预配置密码。输入密码会触发 15 秒钟的宽限期，在此期间不会再次触发警报。

它可能没有三层厚的钢门和热传感器，但它是满足简单需求的简单设备。以目前的形式来看，它可能非常有用，只要稍加修改，它就可以有广泛的用途。

继续阅读，观看绊网报警器的演示视频，并确保查看其他基于[绊网的](http://hackaday.com/2010/04/08/intruder-alarm-mcdonalds-hacking/) [安全系统](http://hackaday.com/2010/01/03/arduino-security-with-frickin-laser/)。

[https://www.youtube.com/embed/vIzUUX8hrEI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/vIzUUX8hrEI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)