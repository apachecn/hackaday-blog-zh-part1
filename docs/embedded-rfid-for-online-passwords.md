# 用于在线密码的嵌入式 RFID

> 原文：<https://hackaday.com/2010/10/11/embedded-rfid-for-online-passwords/>

![](img/46203be332f6651aaab6e29b6b0e01f5.png "implanted-rfid-passwords")

[Jair2K4]正在使用他的唯一 RFID 标签地址作为在线密码。我们敢打赌，如果你走得足够远，手里有一个植入物，你会不断地寻找使用它的理由。想要做的不仅仅是[挥挥手启动他的汽车](http://hackaday.com/2010/01/14/start-the-car-with-a-wave-of-your-hand/)，他用 Arduino 和视差 RFID 阅读器构建了一个接口模块。他在 Windows 7 上使用一个名为 [AAC Keys](http://www.aacinstitute.org/downloads/aackeys/AACKeys.html) 的程序，模拟了一个使用 Arduino 输入的键盘。当需要登录时，他输入用户名并将光标停在密码框中。通过将 RFID 植入物放在阅读器旁边，ID 作为密码连同提交登录的换行符(可能是回车，我们不确定)一起被转储。休息之后你自己看吧。

一方面，没有人能够像偷钥匙圈上的标签那样容易地偷到他的标签。但是我们知道 RFID 因虚假的安全感而臭名昭著。只要你不把它用于国家机密，我们认为这是一个很好的解决方案。

**更新:**看了这个功能的评论后，【Jair2K4】对自己的代码做了一些修改。它现在读取标签，并用存储的数据验证它，然后吐出你想要的任何密码(使得不时地改变密码变得容易)。他还在草图中加入了伺服控制。

[https://www.youtube.com/embed/W6FRRaWo60w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=32&wmode=transparent](https://www.youtube.com/embed/W6FRRaWo60w?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&start=32&wmode=transparent)