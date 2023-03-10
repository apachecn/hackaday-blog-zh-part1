# 从“无法初始化 HAL”错误中恢复 Acer Aspire One

> 原文：<https://hackaday.com/2011/03/04/recover-acer-aspire-one-from-failed-to-initialize-hal-error/>

![](img/86dbfca28157a8091ce3bdbe8d9bcca4.png "aao-failed-to-initialize-hal")

宏碁 Aspire One 是一款上网本，通常预装 Linux 操作系统。这对开源爱好者来说很好，因为市场份额是根据出货量计算的，而不是用户购买硬件后安装的东西。不幸的是，有一个相当大的缺陷会导致“初始化 HAL 失败”的错误，如上所示。[Michael Crummy]提出了一组步骤，您可以使用这些步骤从这个错误中恢复过来。

那么这个错误是什么呢？HAL 代表[硬件抽象层](http://en.wikipedia.org/wiki/Hardware_abstraction_layer)，它允许一个用户界面与许多不同类型的硬件进行通信。如果你自豪地拥有一台 Aspire One，并被这个错误所震惊，你会突然发现你不能再使用 USB 端口、读卡器、有线或无线网络连接器或声卡。因此，您无法连接到互联网，也无法从使用当前安装的操作系统的设备上获取任何文件。对于一个[尼尔·斯蒂芬森] [曾形容为](http://artlung.com/smorgasborg/C_R_Y_P_T_O_N_O_M_I_C_O_N.shtml)“就像美国陆军的 M1 坦克，由太空时代的材料制成，塞满了尖端技术”的操作系统来说，这是一个非常大的问题。

我们知道你在想什么…从 u 盘上启动一个实时会话，从硬盘上获取你需要的东西。这一切都很好，但是你不应该被迫全新安装 Linux 来解决问题。因此，检查[迈克尔的]方法，并确保您关闭宏基实时更新服务器，这很可能是问题的原因。