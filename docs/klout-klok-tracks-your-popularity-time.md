# Klout Klok 追踪你的受欢迎程度，时间

> 原文：<https://hackaday.com/2011/07/21/klout-klok-tracks-your-popularity-time/>

[![](img/41a6dfa8fb2a5372c7a7d2053d014ac1.png "klout")](http://hackaday.com/wp-content/uploads/2011/07/klout.png)

[杨奇煜·罗耶]一直在玩 Netduinos，他刚刚想出了一个非常棒的项目，将显示时间和社交媒体受欢迎程度。这是一个非常好的建设，我们猜测他的社交媒体影响力将很快上升。

Klout 是一项连接到你的脸书或推特个人资料的服务，它会告诉你在 1 到 100 的范围内你有多大的影响力(可能是 10 到 100。见[这个](http://wp.me/p1qlPN-1V)。为了构建 Klout Klock [Fabian]使用了一个 [Netduino Plus](http://www.netduino.com/netduinoplus/specs.htm) ，这是一个很好的选择，因为它集成了以太网端口。Netduino 连接到 [Klout API](http://developer.klout.com/api_gallery) 以满足虚荣心或承认声望。显示器是一个苹果 [TFT 屏幕](http://www.adafruit.com/products/358)。

这个版本真正有趣的地方是对 Netduino 内存限制的处理。该项目不仅要为显示存储 40kb，还要更新内部时钟，获取并解析 Klout 指标，最终显示所有内容。[Fabian]通过在 Netduino 上使用 SD 卡作为虚拟内存，解决了屏幕缓冲问题。

从 Klout 下载的数据完全是另一回事——标准。Net micro frameworks 占用了太多的 RAM，因此该项目仅通过简单的套接字连接来连接 Klout 服务器，并将所有内容存储到 SD 卡中。[Fabian]也找不到轻量级的 JSON 解析器，所以他最终自己写了一个。所有的东西都被编码成尽可能的轻量级，所以最终的版本是一个像 C 程序一样编写的 C++应用程序。

看看下面的视频。

[https://www.youtube.com/embed/MYyiglSI6iw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/MYyiglSI6iw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)