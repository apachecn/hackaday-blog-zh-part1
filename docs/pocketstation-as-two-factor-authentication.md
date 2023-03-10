# PocketStation 作为双因素身份验证

> 原文：<https://hackaday.com/2011/10/30/pocketstation-as-two-factor-authentication/>

![](img/7bedd0a424408ae5d637dd7f8f0b11b6.png "pocketstation")

[DarkFader]发送了他在索尼 PocketStation 上实现双因素认证[的构建。](http://darkfader.blogspot.com/2011/10/pocketstation-google-authenticator.html)

[PocketStation](http://en.wikipedia.org/wiki/PocketStation) 是 PS1 的配件，旨在成为 [Dreamcast VMU](http://en.wikipedia.org/wiki/VMU) 的竞争对手。[DarkFader]用一个神话般的 [PocketStation 模拟器](http://www.ngemu.com/122312/pocketstation-emulator-pk201-released)为他的 PocketStation 编写了一个应用程序，并用 PS3 存储卡适配器和 [MCRWwin](http://www.geocities.jp/altshibabou/win/MCRWwin.html) 上传。

PocketStation 应用程序(此处[可用](http://files.darkfader.net/ps/files/auth.compiled.zip))获取一个密钥，并将其与当前时间进行哈希运算，以生成一个六位数的代码。结合[谷歌对](http://googleblog.blogspot.com/2011/02/advanced-sign-in-security-for-your.html)双因素认证的支持，[DarkFader]的存储卡提供了访问他的谷歌个人资料。

双因素认证也用于今年早些时候[泄露](http://bits.blogs.nytimes.com/2011/04/02/the-rsa-hack-how-they-did-it/)的 [RSA SecurID](http://en.wikipedia.org/wiki/SecurID) 密钥卡。这导致[大量](http://money.cnn.com/2011/10/27/technology/rsa_hack_widespread/)公司被渗透。对于一个人来说，默默无闻是一种合理的(但最终仍然是徒劳的)提供更多安全的方式，但 PocketStation 黑客仍然非常酷。

休息之后，请观看显示[DarkFader]使用其 PocketStation 令牌的视频。

[https://www.youtube.com/embed/3echEnfSEfE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/3echEnfSEfE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)