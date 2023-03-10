# 打造史上最差的 Linux PC

> 原文：<https://hackaday.com/2012/03/28/building-the-worst-linux-pc-ever/>

Linux 通常被认为是低功率计算机的首选操作系统。想要挑战 Linux 需要“过去 20 年制造的计算机”这一先入为主的观念，【Dmitry】围绕一个简单的 8 位微控制器构建了[有史以来最差的 Linux PC](http://dmitry.co/index.php?p=./04.Thoughts/07.%20Linux%20on%208bit)。

所用的 ATMega1284p [Dmitry]在 RAM 和存储方面没有太大的优势；只有 16 千字节的 SRAM 和微不足道的 128 千字节的闪存。虽然这在嵌入式世界中可能是巨大的，但与即使是低端上网本上的千兆字节 RAM 和硬盘空间相比，这只是沧海一粟。为了解决这个问题，[Dmitry]抛出了一个古董 30 针 RAM SIMM。它直接连接到微控制器上，就像作为电脑硬盘的 1gbsd 卡一样。

Linux 需要一个 32 位的 CPU 和一个内存管理单元，这是微控制器所没有的。对[Dmitry]来说，最好的做法是在 AVR 上模拟 ARM 处理器。我们不确定这是天才还是疯子，但事实证明这是编写模块化 ARM 仿真器的一次有价值的学习。

有多快？[Dmitry]告诉我们启动 bash 提示符需要两个小时，加载 Ubuntu 并登录需要四个多小时。如果你想要兆赫等级，祝你好运；有效时钟速度约为 6.5 *千赫。虽然有史以来最差的 Linux 个人电脑不会赢得任何比赛，但它简单的结构使它即使是最笨拙的硬件建造者也能做到；整个设备只是一个微控制器、RAM、SD 卡、几个电阻和一些导线。*

如果你想构建自己最差的 Linux PC，[Dmitry]有固件和磁盘映像可供下载。如果你想看这个东西开机的~~延时~~，可以看看休息后的视频。

[https://player.vimeo.com/video/39286771](https://player.vimeo.com/video/39286771)