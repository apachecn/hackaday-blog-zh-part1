# 如何:SSH HTTP 代理设置

> 原文：<https://hackaday.com/2005/08/31/how-to-ssh-http-proxy-setup/>

![putty config](img/b98725e4480005a2256f8d106192024a.png)

我们最近在链接帖子中链接了几个代理选项，[tom]认为写下如何使用 [Privoxy](http://www.privoxy.org/) 是个好主意。在[tom]的案例中，他想通过一个加密的隧道将他在工作中的所有网上冲浪路由到他的家用机器。该指南是基于 Windows 的，但是翻译成你选择的操作系统不会太难。首先在家用机器上设置一个 [OpenSSH](http://sshwindows.sourceforge.net/) 服务器和新用户。然后安装 Privoxy。接下来[油灰](http://www.chiark.greenend.org.uk/%7Esgtatham/putty/)用于建立从工作机械的安全通道。最后一步是配置浏览器使用代理。你也可以用这个做即时消息。你可能在工作或学校不需要这个，但是如果你在外面使用开放的接入点，它应该可以为你提供一些不错的保护。

*   [永久链接](http://www.zunta.org/blog/archives/004498.php)