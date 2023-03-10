# 使用蓝牙和视频流进行远程电话控制

> 原文：<https://hackaday.com/2011/02/27/remote-phone-control-using-bluetooth-and-a-video-stream/>

![remote_bluetooth_phone_control](img/aaa2feeab237c68358d5c74467565e5d.png "remote_bluetooth_phone_control")

一日黑客读者[Bobbie]发给我们一个黑客，这是我们本周早些时候介绍的[自动手机按键机](http://hackaday.com/2011/02/24/machine-pushes-cellphone-buttons-from-anywhere-in-the-world/)的改编版。受那个项目的启发，他挑战自己，想出一个更有效的方法来解决这个问题。

他以几乎相同的方式开始，将摄像头对准手机，以便远程查看显示屏。他致力于使他的项目与众不同的主要原因是手机上的按钮被激活的方式。他对机械按钮按压装置印象深刻，但认为它过于复杂。相反，他决定通过蓝牙将按键发送到他的手机上，而他的手机恰好兼容 AT+CKPD。

不仅如此，他的界面也令人印象深刻。原本计划使用键盘向手机发送输入，他改变了路线，将他的视频流 GUI 编程为记录鼠标点击。现在，当他点击视频显示中的一个手机按钮时，相应的按键就会发送到手机上——太棒了！

继续阅读，看看他的远程电话接口的视频，你会很高兴你做到了。

[https://www.youtube.com/embed/-HEqURMyqNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/-HEqURMyqNA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)