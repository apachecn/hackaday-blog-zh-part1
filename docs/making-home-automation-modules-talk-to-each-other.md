# 让家庭自动化模块相互交流

> 原文：<https://hackaday.com/2010/08/04/making-home-automation-modules-talk-to-each-other/>

![](img/bc1076ea1715c737c1fa14fddcf55724.png "rnet-to-sonos-bridge")
【Danny】一直在做[一座 RNET 到索诺斯的桥](http://www.mavromatic.com/2010/07/russound-rnet-to-sonos-bridge/)。这些设备来自两家不同的制造商，用于为全屋音频系统提供便利。通常有一个带大彩色屏幕的主控制器，然后是几个卫星控制器，如上图所示，它们具有一些功能，但成本较低。通常情况下，你只能使用一系列设备中的硬件来让它们相互通话，但(丹尼)对这种限制说“没门”。

他的最新帖子详细介绍了他是如何实现这一目标的。他用一个带有 Arduino 的 RS232 串行接口来嗅出来自 RNET 基站的数据流。一旦他弄清楚了协议，他就使用 Arduino 来解析所有传入的命令，为 Sonos 控制器格式化它们，并通过以太网电缆将其发送到该设备。他把所有的东西都绑在一起，并且在工作。休息后看看剪辑中的证明。

[https://www.youtube.com/embed/Hzj6kTAB5K4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Hzj6kTAB5K4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)