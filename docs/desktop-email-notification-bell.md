# 桌面电子邮件通知铃

> 原文：<https://hackaday.com/2011/07/24/desktop-email-notification-bell/>

![email_notification_bell](img/4a622c9fcec6406114b68622e34af96e.png "email_notification_bell")

Instructables 用户[meseta]希望在收到电子邮件时收到声音通知，但他肯定认为自己的计算机内置声音在某些方面有所欠缺。为了获得他想要的完美声音，他给自己做了一个 USB 供电的通知铃。

利用现成的“前台铃”和一个手工制作的电磁铁，他建造了一个铃，每当有消息出现在他的桌面电子邮件客户端时，这个铃就会被触发。电磁体可以由微控制器的快速脉冲触发，在[meseta 的]案例中，他使用了前脑开发板。他在自己的电子邮件客户端中创建了一个过滤器，每当收到一封邮件时就会运行一个可执行文件。这个可执行程序反过来通过 USB 向他的微控制器发送信息，触发铃声。

虽然我们认为可以用一个功能弱得多的微控制器来组装通知程序，但不管怎样，这是一个好主意。人们似乎喜欢[替代](http://hackaday.com/2009/11/06/physical-email-notification/) [通知](http://hackaday.com/2009/09/05/arduino-email-alert/) [系统](http://hackaday.com/2008/09/28/email-notification-via-an-rgb-led/)，所以我们很确定这个铃声会吸引人群中的许多人。

请继续阅读，观看他的电子邮件通知程序的视频短片。

[https://www.youtube.com/embed/flgRRSD1ycI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/flgRRSD1ycI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)