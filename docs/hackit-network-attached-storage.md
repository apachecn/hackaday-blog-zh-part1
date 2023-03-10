# Hackit:网络附加存储？

> 原文：<https://hackaday.com/2008/07/05/hackit-network-attached-storage/>

随着每一天的过去，我们获取数字媒体的速度都在增加(当我们搬家的时候，甚至都懒得打开我们的 CD)。大型出版商已经开始远离 DRM，这意味着我们将来会购买更多的数字媒体。获得所有这些非物质的财产，不仅要让它容易获得，还要保护它不被破坏。 [Slashdot 向](http://ask.slashdot.org/article.pl?sid=08/06/30/1411229)询问读者关于购买什么 NAS 的建议；我们收集了下面的一些选项，想知道你用的是什么。

对于那些愿意自己构建机器的人来说，有几个以 NAS 为中心的发行版可供使用。FreeNAS 基于 FreeBSD，占用空间不到 32MB，尽管它有一个全功能的网络界面。 [Openfiler](http://openfiler.com/) 可用于构建成熟的 NAS/SAN 设备。它可以部署在裸机上或作为虚拟机，2.3 版具有绑定多个网卡等新功能。 [CryptoNAS](http://cryptonas.org/) 是一个 liveCD，帮助你建立一个用户友好的 NAS 设备，具有完全的硬盘加密功能。

许多消费者 NAS 设备已经选择运行 Linux。这使得它们成为添加新功能的很好的攻击目标，我们在过去已经讨论过很多。Linksys NSLU2“slug”已经非常受欢迎。Buffalo 已经出售了许多不同的设备:[Kurobox、Linkstation 和 Terastation](http://buffalo.nas-central.org/index.php/Main_Page) 都有专门的改装社区。我们的办公室里有一个 [LaCie 以太网迷你磁盘](http://luon.net/~admar/journal/LaCieEthernetDiskMini.html)没有打开，最初购买它是因为我们知道它们可能会被黑客攻击。NAS-Central 列出了许多其他专门针对 NAS 设备的在线社区。

对多管理一台 Linux 机器不感到兴奋吗？当苹果在今年早些时候发布时间胶囊时，它向世界介绍了“刚刚工作”的高容量存储。虽然[不完全是服务器级的](http://www.bit-tech.net/news/2008/03/03/apple_time_capsule_not_server_grade/1)，但它给家庭用户带来了定期备份的理念。1TB 很好，但它不可升级，也不容易更换；看看 [Drobo](http://www.drobo.com/) 就知道了。Drobo 通过让任何人都能轻松管理存储建立了一个粉丝群。只需将您的商品驱动器扔进箱子，您就可以开始了。不幸的是，将其转换为 NAS 需要额外支付 200 美元。他们已经[发布了一个 SDK](http://www.drobospace.com/page/developers) ，所以你应该很快就会看到新的应用程序。

所有这些选项都只是针对内部服务，但没有一个是真正的备份解决方案，因为当你的房子被烧毁时，你的数据仍然会消失。几年前，[Jeremy Zawodny]调查了将他的备份服务器转移到亚马逊的 S3 的情况，并汇编了一份与该服务配合使用的工具的[列表。](http://jeremy.zawodny.com/blog/archives/007641.html)[丛林磁盘](http://jungledisk.com/)可能是对用户最友好的。它是多平台的，可以作为本地磁盘安装。Windows Home Server 也有一个加载项。如果你想建立一个简单的个人备份系统，我们强烈推荐[jwz]的[定期备份建议](http://jwz.livejournal.com/801607.html)。

这是一个相当全面的黑客友好的备份选项，但我们想知道你用什么。您如何存储、服务和保护您的数据？您为商用 NAS 设备添加了哪些定制功能？