# 使用升级内部存储的 Chumby Webserver

> 原文：<https://hackaday.com/2010/11/29/chumby-webserver-using-upgraded-internal-storage/>

![](img/22a827cf2c0c79420ca838a203003fef.png "chumby-webserver")

Chumby One 内置 SD 卡，提供相当大的存储空间。(肯尼斯·芬尼根的)配有一个 1 GB 的卡，还有大约 500 MB 的剩余空间，他在里面放满了一堆 MP3。但是他想做得更多，所以安装了一个预编译版本的 lighttpd 作为网络服务器。问题是这个二进制文件需要插入一个拇指驱动器，因为它将存储目录映射到挂载的 USB 文件夹。他对此并不满意，所以他[升级了内部 SD 卡，并推出了自己的网络服务器](http://kennethfinnegan.blogspot.com/2010/11/chumby-webserver-without-flash-drive.html)从内部 SD 卡上运行。

升级包括从 1 GB 升级到 8 GB 的 microSD 卡。为了在内部运行 web 服务器，他需要重新编译 lighttpd 以使用不同的根目录。这意味着建立一个 ARM 交叉编译器，并最终为启动脚本找到一个新的位置。“lighty”目录的位置变化让我们怀疑，如果不重新编译，符号链接是否不能解决这个问题。但是我们手头没有硬件来亲自试验。

但是如果你想尝试一下，可以看看[Bunnie 的]关于基于 Chumby 的硬件的帖子。看起来你可以去大盒子商店买一个，而不用剥太多蛤蜊。