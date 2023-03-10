# 工具 9: URI 使用和滥用

> 原文：<https://hackaday.com/2007/10/21/toorcon-9-uri-use-and-abuse/>

![](img/5e90f346cd00fbcf617cb9b2f3791c1c.png)
【Nathan McFeters】和【Rob Carter】做了一个关于 URI 处理问题的报告。URIs 用于从 web 浏览器向外部应用程序发送命令。比如 iTunes 的 itms://。任何注册了 URI 的应用程序都有可能通过这种途径被滥用。在第一个例子中，他们展示了 Trillian 的 AIM 处理中的堆栈溢出。下一个演示在 Picasa 的界面上创建了一个“关键更新可用”按钮。当用户点击它时，他们的照片会被上传到攻击者的服务器上。他们甚至显示一个“下载进度”栏来鼓励用户保持连接畅通。你可以在[的共同出资人比利·里奥斯的博客](http://xs-sniper.com/blog/Picasa-URI/)上读到这次袭击。

*   [永久链接](http://xs-sniper.com/blog/Picasa-URI/)