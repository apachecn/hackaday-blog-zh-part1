# Shmoocon 2006: Wi-Fi 欺骗或如何保护，破坏和享受 Wi-Fi 的乐趣

> 原文：<https://hackaday.com/2006/01/30/shmoocon-2006-wi-fi-trickery-or-how-to-secure-break-and-have-fun-with-wi-fi/>

![shmoocon](img/88236af7f00f1ab3e122a4bb8c568266.png)

来自法国电信 R&D 公司的 Franck Veysset 和 Laurent Butti 在 Shmoocon 上展示了几款使用 802.11 原始注入的概念验证工具。首先是[生假 AP](http://rfakeap.tuxfamily.org/#Raw_Fake_AP) 。最初的[假 AP](http://www.blackalchemy.to/project/fakeap/) 是一个生成数千个假接入点的脚本。这是很容易发现的，因为像 BSSID 这样的指示信号显示 AP 只启动了几毫秒。原始的假 AP 试图通过修改 BSSIDs 并以一致的时间间隔发送信标帧来生成合法的接入点。

[Raw Glue AP](http://rfakeap.tuxfamily.org/#Raw_Glue_AP) 设计用于捕获来自客户端的探测请求，扫描首选 ESSID。然后，它会尝试生成适当的探测响应，让客户端保持忙碌。

原始秘密是最后的工具。它在有效的 ACK 帧内创建一个隐蔽通道。ACK 帧通常被认为是无害的，会被无线 IDS 忽略。这个工具现在真的很简单，没有加密，也不能处理丢帧。

*   [永久链接](http://rfakeap.tuxfamily.org/)