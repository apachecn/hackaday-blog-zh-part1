# FUSE:用户空间中的文件系统

> 原文：<https://hackaday.com/2005/11/11/fuse-filesystem-in-userspace/>

![flickr](img/bda3786b7fd8dd770ac7ac235fc61ff1.png)

本周有很多关于 Flickr 的虚拟文件系统的讨论。使用 Flickrfs，你可以像普通文件系统一样与 Flickr 标签和照片进行交互。一个类似的服务是 [GmailFS](http://richard.jones.name/google-hacks/gmail-filesystem/gmail-filesystem.html) ，它让你把一个 Gmail 账户作为一个大的虚拟文件系统。这两个服务都是建立在 [FUSE](http://fuse.sourceforge.net/) 之上的。FUSE 使得在用户空间程序中构建全功能文件系统变得容易。用户可以编写脚本和操作文件，就像他们的常规文件一样。FUSE 现在是主 Linux 内核的一部分，发布版本为 2.6.14 。查看使用 FUSE 构建的其他有趣的[文件系统列表。特别关注:](http://fuse.sourceforge.net/wiki/index.php/FileSystems) [WikipediaFS](http://wikipediafs.sourceforge.net/) ， [SMB for FUSE](http://hannibal.lr-s.tudelft.nl/fusesmb/) 类似于网络邻居， [SSHFS](http://fuse.sourceforge.net/sshfs.html) ， [btslave](http://btslave.sourceforge.net/) 挂载 torrent 文件， [djmount](http://djmount.sourceforge.net/) 是 UPnP AV 客户端。

*   [永久链接](http://fuse.sourceforge.net/)