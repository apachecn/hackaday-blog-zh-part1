# 将 Twitter 放入 VFD 时钟中

> 原文：<https://hackaday.com/2011/09/29/putting-twitter-in-a-vfd-clock/>

![](img/3cdc8da97160be2355ffe81b43d24be5.png "hello")

不满足于只知道时间，[trandi]决定他的真空荧光显示时钟会好得多，如果它能显示天气和推特信息。

[trandi]上个月收到了一个 Lady Ada [冰管钟](http://www.ladyada.net/make/icetube/index.html)。这个工具包几乎太容易组合在一起了。现在他必须“让它连接到其他‘东西’并显示一些自定义信息。”在玩了显示 Hello World 的固件后，[trandi]摆弄了一下 [GPS 模块](http://www.ladyada.net/make/icetube/mods.html)，并想出了如何在串行连接上添加[滚动文本。](http://www.youtube.com/watch?v=iftO821zaWA)

与联网计算机的串行连接固然很好，但[trandi]真的想要一个独立的解决方案。一个连接 RS-232 板的微型 WiFi 被找到，在互联网上获得时钟的工作开始认真进行。在浪费了一个周末的时间尝试调试 WiFi 板的 HTTP 模式后，【trandi】放弃了，使用 TCP 模式，手动构造 HTTP 头。

时钟获取当前天气和 Twitter 信息。为了超越艾斯·库伯 GPS 模块，这个时钟现在可以从互联网上设置自己的时间。休息之后，看看[trandi]展示他的互联网时钟和精美的单麦芽威士忌收藏的视频。

[https://www.youtube.com/embed/ZjUhav5uDgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ZjUhav5uDgE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)