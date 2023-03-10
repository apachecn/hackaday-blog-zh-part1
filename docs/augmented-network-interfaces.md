# 增强的网络接口

> 原文：<https://hackaday.com/2009/04/25/augmented-network-interfaces/>

![agarwal-nsdi09-somniloquypdf-page-7-of-16](img/d379fb737ac93a1548e1ca000de5e214.png "agarwal-nsdi09-somniloquypdf-page-7-of-16")

这是微软和加州大学圣迭戈分校的一项有趣的研究。梦语项目是一种新型的网络接口。它是一个 USB 设备，允许计算机在进入睡眠状态后继续进行网络通信。通过卸载这些任务，通常会因 RDP 和文件传输而保持唤醒状态的机器仅在绝对必要时才会启动。该设备使用类似于 [Tor 硬件适配器](http://hackaday.com/2008/12/21/tor-hardware-privacy-adapter/ "Tor hardware privacy adapter  - Hack a Day")中使用的 Gumstix 板。上图的设备有两个 USB 接口，但第二个只是为了调试，并不需要正常运行。该板运行 BSD 并创建一个到 Vista 主机的 USBNet 桥。当主机守护程序检测到计算机进入睡眠状态时，它会将活动通信传递给 gumstix。他们开发了“存根”应用程序来处理各种类型的通信。对于下载，他们使用 wget 只下载剩下的那部分数据。对于 bittorrent，他们定制了命令行客户端 ctorrent 来管理下载。两个程序在完成后都会唤醒电脑，并将文件从 SD 卡中转移出来。

[via [Engadget](http://www.engadget.com/2009/04/25/somniloquy-external-networking-card-lets-pcs-sleep-talk-essent/ "Somniloquy external networking card lets PCS ")