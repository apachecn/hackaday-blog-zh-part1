# 在惠普触摸板上安装 OpenSSH

> 原文：<https://hackaday.com/2011/08/26/installing-openssh-on-the-hp-touchpad/>

![hptouchpad_openssh](img/18208cfb43c9ead992c6e9ad53ad26ce.png "hptouchpad_openssh")

[Russ]很幸运地得到了一个折扣很高的 HP TouchPad，在听说为在该设备上运行 Android 提供了巨额奖金后，他决定四处逛逛，看看他是否能取得一些进展。

他首先使用惠普 WebOS 网站上的工具制作了文件系统的完整备份副本，以防在此过程中他的设备发生任何不幸。他抓起一份 ARM 交叉编译器，着手为 TouchPad 构建一份 OpenSSH。一旦有了二进制文件，他就开始了他认为将 SSH 安装到触摸板上的艰苦过程，但结果证明这只是一个简单的拖放操作。

在重新安装文件系统以允许写操作之后，他启动了 SSH 守护进程，并希望一切顺利。它非常有效，虽然它是让 Android 在触摸板上运行的相对较小的一部分，但每一点都有帮助。