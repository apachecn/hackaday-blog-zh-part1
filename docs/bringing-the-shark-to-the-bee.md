# 把鲨鱼带给蜜蜂

> 原文：<https://hackaday.com/2010/12/29/bringing-the-shark-to-the-bee/>

![](img/f6c4df4fecd8e1d89b06bea94c0d285b.png "FreakShark")

Wireshark 是公认的最好的网络分析工具之一，长期以来一直被合法的网络专业人员以及更阴暗的人群(以及两者之间的任何地方)所使用。虽然对分析有线和 Wi-Fi 流量很有用，但监控 802.15.4 协议(如 Zigbee)在过去并不常见。FreakLabs 的[Akiba]为我们带来了一个解决方案[，它绕过了 Wireshark 的 libpcap 基础的正常限制，不接受大多数使用 FTDI 或 Arduinos 连接到](http://freaklabs.org/index.php/Tutorials/Software/Feeding-the-Shark-Turning-the-Freakduino-into-a-Realtime-Wireless-Protocol-Analyzer-with-Wireshark.html) [Zigbee](http://hackaday.com/2008/11/02/wireless-arduino-programming-with-zigbee/) [设备](http://hackaday.com/2009/12/21/hacking-zigbee-chips-cc2430/)的自制程序设置的简单串行输入。使用命名管道和一些自定义脚本，[Akiba]已经能够哄骗 Wireshark 接受来自 FreakLabs Freakduino 板之一的输入。

虽然确实有直接连接到 Wireshark 的专业无线分析工具，但我们 Hackaday 喜欢炫耀任何人，他们采用困难、廉价、不碍事的方法做事情，而不是整洁、昂贵的商业方法。