# 可启动 USB RAM 捕获

> 原文：<https://hackaday.com/2008/03/03/bootable-usb-ram-capture/>

![](img/3e2e0b3a4f203709b03ce53a2fa95398.png)
受到在[普林斯顿](http://digg.com/security/Cold_Boot_Attacks_on_Windows_Vista_BitLocker_Encryption_Keys)(看起来原来的网站关闭了)所做的一些研究的启发，【韦斯利】在[发送了他的](http://mcgrewsecurity.com/projects/msramdmp/)版本的可引导 RAM 转储 USB 驱动器，并附有一份如何自己滚动的指南。他组装了一个在 syslinux 下运行的实用程序来捕获数据，将其安装到 USB 拇指驱动器上，并设法创建了一个可以在机器上启动的设备，并在 RAM 的内容被另一个实用程序覆盖之前复制它。

*   [永久链接](http://mcgrewsecurity.com/projects/msramdmp/)