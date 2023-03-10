# NAS 固件黑客:运行在 QNAP 硬件上的 Synology

> 原文：<https://hackaday.com/2012/01/31/nas-firmware-hack-synology-running-on-qnap-hardware/>

![](img/17b02f60333e8cecb22b12e8f77647e7.png "qnology")

[XVortex]完成了一次相当不可思议的固件破解。他设法为运行在 QNAP 机器上的 Synology 升级了固件。这两个都是网络连接存储设备，但显然 Synology 固件比 QNAP 提供的产品更好。

好的一面是，这不是一次性的攻击。你可以下载原始图像，并给自己一个旋转。不过，还是要提醒你几句。它只能在使用 Atom 和 ICH9R 芯片组的型号上工作，如果你有一个配备 ARM 处理器的型号，你就不走运了。新固件刷新后，您还需要格式化驱动器，因此，在填满驱动器之前，请进行格式化。

这可以追溯到 DD-WRT 第一次在 Linksys 路由器上运行的时候。我们不记得这是从像这次使用的升级镜像攻击开始的，还是源代码是可用的(一旦证明 Linksys 违反了 GPL，他们就被迫发布它)。

休息之后，请观看这一黑客攻击的证明视频。

[https://www.youtube.com/embed/yg17gW40jgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yg17gW40jgk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[感谢 ZeroQI]