# 使用 RAM 转储打破磁盘加密

> 原文：<https://hackaday.com/2008/02/21/breaking-disk-encryption-with-ram-dumps/>

<http://www.youtube.com/v/JDaicPIgn9U&amp;rel=1>

  
如果你还没有机会，就做[观看这次攻击的视频](http://www.youtube.com/watch?v=JDaicPIgn9U)。它很好地解释了这个问题。计算机开机时，全驱动器加密将密钥存储在 RAM 中。当断电时，RAM 中存储的数据不会立即消失，而是会随着时间的推移而消失。为了找回密钥，他们关掉了电脑，从一个创建了内存镜像的 u 盘启动。你可以在这里阅读更多关于攻击[的信息。](http://citp.princeton.edu/memory/)

如何减少这种威胁？您可以关闭 USB 引导，然后在 BIOS 上设置密码，以防止视频中显示的特定活动。此外，您可以加密磁盘上文件夹中很少使用的数据。他们仍然可以解密磁盘，但他们不会得到一切。我不认为这个问题会得到真正的解决，除非在硬件设计上有一个根本性的改变来清除内存，即使这样，它也可能只会帮助那些关机的电脑，而不是挂起的电脑。

这种攻击的可能性一直被谈论，我很高兴看到有人成功了。我希望看到未来对使用带 DMA 访问的 USB/ExpressCard 转储 RAM 数据的研究。

*   [永久链接](http://citp.princeton.edu/memory/)