# 用遥控器控制您的电脑

> 原文：<https://hackaday.com/2012/03/05/control-your-pc-with-a-remote/>

![](img/215425d113158dd18f30d69ac19b1ec1.png "remote")

因为他的计算机正在逐渐变成一个包罗万象的媒体显示设备，[Shawn]认为一个控制音量的遥控器和一个视频播放列表将是一个合理的补充。电脑用的电视遥控器已经问世多年了，但是[Shawn]决定走 DIY 路线，制作自己的电脑遥控器。

为了构建，[Shawn]使用了一个 [Teensy 开发板](http://www.pjrc.com/store/teensy.html)和一个 IR 接收器模块以及必要的[红外远程库](http://www.pjrc.com/teensy/td_libs_IRremote.html)。为了将红外信号转换成键盘命令，[Shawn]决定将他的项目建立在[之前的版本](http://dan.hersam.com/2010/05/06/mute-and-adjust-volume-with-keyboard-hotkeys/)的基础上，该版本使用了一个名为 AutoHotKey 的小程序。

现在，构建可以在预定义的 YouTube 和 Shoutcast 播放列表中循环，并改变当前播放曲目的音量。也支持用遥控器上的方向按钮移动鼠标，但我们想知道是否更好的实现是使用 [Windows 多媒体键盘扫描码](http://www.computer-engineering.org/ps2keyboard/scancodes2.html)，即【Shawn】的笔记本电脑应该支持*。*

尽管如此，[肖恩]设法做了一个非常好的构建，非常适合我们的计算机战斗站。休息之后，请查看遥控器的运行演示。

[https://www.youtube.com/embed/3O6VygUv7Qg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3O6VygUv7Qg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)