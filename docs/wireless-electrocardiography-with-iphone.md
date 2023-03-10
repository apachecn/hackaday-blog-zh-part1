# 无线心电图…使用 IPhone

> 原文：<https://hackaday.com/2010/09/27/wireless-electrocardiography-with-iphone/>

![](img/c4d6a73a045345b40e3eb485017f0a6b.png "wireless-ecg")

这个模块[是一个传感器包，用于监测心脏](http://esl.epfl.ch/page-42817.html)的电活动。它是努力创造一个无线身体传感器网络节点的产物，该节点是[可靠的，同时消耗非常少的电力](http://esl.epfl.ch/page-42437.html)，这意味着更长的电池寿命。为了实现这一点，负责节点的微控制器会压缩数据(无线 ECG 硬件通常不会这样做)，以使无线电传输尽可能短且不频繁。

[Igor]向我们发送了这个提示，并与其中一名开发人员进行了简短的问答。似乎他们现在正在使用 MSP430 芯片，因为它们的功耗很低。不幸的是，这些芯片在传输时仍然会产生很高的负载，因此未来的版本将会使用替代方案。

哦，为什么是 iPhone？显示数据的设备没什么区别。在这种情况下，他们通过蓝牙传输实时显示(在休息后的视频中可以看到)。这可以用于各种各样的设备，或通过互联网远程监控。

[https://www.youtube.com/embed/iURXzBsckOc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iURXzBsckOc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)