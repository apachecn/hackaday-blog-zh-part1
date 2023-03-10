# 通过取消认证数据包的 WiFi 干扰

> 原文：<https://hackaday.com/2011/10/04/wifi-jamming-via-deauthentication-packets/>

[Elliot]整理了一个有趣的概念验证脚本，它使用[重复的身份验证数据包突发来干扰 WiFi](http://code.google.com/p/wifijammer/) 接入点。据我们所知，这是使用旧工具的新方法。Aircrack-ng 是[在 WiFi 黑客](http://hackaday.com/2010/10/07/an-interesting-take-on-wep-cracking/)中经常见到的一个包。它包括[一个解除认证命令](http://www.aircrack-ng.org/doku.php?id=deauthentication)，该命令使 WiFi 客户端停止使用接入点并尝试重新认证自己。[Elliot 的]攻击包括重复发送解除身份验证数据包，这实际上从不允许客户端传递任何数据，因为它们总是与身份验证捆绑在一起。

休息之后，你可以看到一个视频演示这是如何工作的。该脚本检测该区域的接入点。攻击者选择要阻塞的部分，然后脚本调用 Aircrack-ng 命令。如果你有关于如何防范这类事情的想法，我们很乐意倾听。请在评论中留下你的想法。

[https://www.youtube.com/embed/RmabhHiQ4yY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RmabhHiQ4yY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)