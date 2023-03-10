# 智能手机操作的车库门是 Arduino 家庭自动化系统的开端

> 原文：<https://hackaday.com/2011/03/20/smartphone-operated-garage-door-is-beginning-of-arduino-home-automation-system/>

![](img/4ac67c5e0f3b6c08c632ff1d374b31ce.png "arduino-garage-door-controller")

[Tim]正在展示他的家庭自动化的第一步，这个智能手机车库门界面。在休息后的视频中，你可以看到他用一个按钮打开和关闭车库门。还有一个打开或关闭的指示器，当他离开家时可以检查。

Arduino 负责这个项目的部分控制。就像我们昨天看到的帖子一样，他在网页上使用 PHP 代码通过 USB 连接操纵 Arduino，以便使用继电器开关门。门的状态也由 Arduino 监控，并通过串行连接发送到 PC。计算机使用 Python 脚本来监控传入的数据，并更新一个文本文件，该文件使用 PHP include 合并到 web 界面中。该系统的未来计划包括增加对供暖和空调系统的控制。

如果你想做这样的事情，但却是无线的，这里有一些关于抛弃 Arduino 并使用 XBee 模块的建议。

[https://www.youtube.com/embed/HfjjA0Gudrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/HfjjA0Gudrg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)