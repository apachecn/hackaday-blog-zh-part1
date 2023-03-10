# ext media:XBMC 换盘机接口

> 原文：<https://hackaday.com/2011/07/15/extmedia-an-xbmc-disc-changer-interface/>

![extmedia_dvd_bluray_changer_integration](img/7c22f0196e4056f04898712924460ddb.png "extmedia_dvd_bluray_changer_integration")

不久前，[本·吉尔斯塔德]建造了他的第一个 HTPC，让 XBMC 在上面管理他所有的数字媒体。他喜欢 XBMC 的功能和灵活性，但他需要一种方式在设备上享受他的 DVD 和蓝光收藏，而没有太多的麻烦。远在[本·赫克]考虑[把他的 Xbox 360 DVD 驱动器装进 CD 转盘](http://hackaday.com/2011/07/12/xbox-360-dvd-changer-is-the-ultimate-in-gaming-laziness/)之前，这个[本]正忙着把一个蓝光播放器装进他的。

他在车库拍卖中买了一个坏了的换碟机，并拆开了一个标准的 SATA 蓝光播放器，为光驱移植做准备。ATMega168 控制换盘机的机械装置，监控转盘的位置，并在需要换盘时触发适当的电机。AVR 目前通过 UDP 代理从 HTPC 的串行端口接收指令，因为 XBMC 在构建转换器时不支持串行接口。

[本的]项目的后半部分是 XBMC 的一个附加物，他用它来管理他的大量光盘收藏。为了让 XBMC 识别出每张光盘都是一个有效的“文件”，他创造了一个巧妙的变通方法，包括空白的 WMV 剪辑。这使他能够观看他的 DVD，就好像它们是他硬盘上的数字文件，带有封面艺术。

这是一个了不起的项目，而且[Ben]说他的系统应该能够同时支持任意数量的物理换碟机，而不会有太大的问题。不幸的是，当他失业后，这个项目就中断了，所以它暂时被封存起来。然而，一旦他重新站起来，他有一个完整的计划改变和改进的列表要做——我们迫不及待地想看到它一旦完成！

请继续阅读，查看他的 XBMC 附加功能的视频演示。

[https://www.youtube.com/embed/p8uq1zcHOrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/p8uq1zcHOrQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)