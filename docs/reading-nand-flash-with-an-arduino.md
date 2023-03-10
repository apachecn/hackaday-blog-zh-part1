# 使用 Arduino 读取 NAND 闪存

> 原文：<https://hackaday.com/2012/01/05/reading-nand-flash-with-an-arduino/>

![](img/7d810e7e23ddb89b466be13fb836c325.png "nand")

[HC]扫视了一下谷歌，看到许多人试图用 Arduino 读取 NAND 闪存芯片。这是个有趣的问题。在 16 兆赫时，[HC]每指令周期大约 60 纳秒，闪存芯片通常运行大约 20 纳秒。他让构建工作起来，并且能够[读取闪存芯片的内存内容和 ID](http://hardcoreforensics.com/arduino-mega-direct-reading-of-a-nand-flash-memory-chip) 。

目前，这只是一个概念验证，以证明读取闪存是可能的。[HC]使用 Arduino Mega 从闪存芯片上提取生产 ID。因为 Arduino 上没有足够的存储空间来容纳数兆字节的数据，所以[HC]正在寻找一种方法来从他的闪存芯片中提取数据。他正在考虑通过以太网发送或者存储在 SD 卡上。

这不是我们第一次看到迂回曲折地使用那些廉价的、无处不在的 NAND 闪存芯片。考虑到我们已经在未使用的拇指驱动器中存放了几十个，因此[HC]的工作显示出了很大的潜力。他在[的论坛上发布了一个话题](http://hardcoreforensics.com/wp/forum/index.php?board=56.0)，看看是否有进一步发展的兴趣，这是我们希望看到的。