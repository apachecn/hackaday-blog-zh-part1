# Arduino 电子邮件提醒

> 原文：<https://hackaday.com/2009/09/05/arduino-email-alert/>

![email](img/dee427fd833d0e08bc1bd06e29c595cd.png "email")

Arduino 为[警报系统](http://hackaday.com/2009/07/27/sewer-clog-alert-system/)提供了一个很好的平台，因为它不需要额外的部件，除了一个 [LED](http://hackaday.com/2009/08/19/moon-phase-light-modification/) 或[电机](http://hackaday.com/2008/10/24/coin-slot-detector/)。[Torchris]制作了[电子邮件通知器](http://opensourceprojects-torchris.blogspot.com/2009/09/arduino-pop3-email-checker.html)，并使用以太网屏蔽使其独立。Arduino 会轮询您的 POP 服务器，查看是否有未读邮件。POP 是一个极其简单的协议，甚至比 HTTP 还要简单；这使得通信变得容易，即使处理能力很低。他希望添加一个伺服或[串行显示器](http://hackaday.com/2009/07/13/parts-4x20-vfd-character-display-na204sd02/)来更好地呈现数据，但他目前的系统似乎工作良好。休息后的视频。

 [https://www.youtube.com/embed/T1nG-naOe2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T1nG-naOe2s?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[via @ [littlebirdceo](http://twitter.com/littlebirdceo/status/3752259134)