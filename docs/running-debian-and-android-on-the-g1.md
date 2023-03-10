# 在 G1 上运行 Debian 和 Android

> 原文：<https://hackaday.com/2008/11/11/running-debian-and-android-on-the-g1/>

![tmobileg1](img/50dd2c797a0c9b418c2209459ae06ff5.png "tmobileg1")

[Jay Freeman]有一个相当详尽的教程，教你如何在你的 T-Mobile G1 上设置 Debian 环境。第一个主要问题是[通过 telnetd](http://hackaday.com/2008/11/09/android-executes-everything-you-type/ "Android executes everything you type  - Hack a Day") 获得根级别的访问正在被修补。这当然是一个需要解决的安全问题，但用户不应该一开始就用自己的手机。虽然 G1 附带了一些 [Linux 工具](http://www.mahalo.com/Linux "Linux - Mahalo")，但它们是有限的。[Jay]的目标是在手机上创建一个熟悉的 Debian 环境。这需要一些技巧，但是如果您熟悉命令行，应该不会有任何问题。Debian 已经支持 ARM EABI，所以创建一个工作映像不成问题。图像文件存储在 SD 卡上，并使用环回设备进行安装。G1 的内核打开了模块支持，所以[Jay]创建了 ext2 和 unionfs 内核模块。【Benno Leslie】的 [Android 版 busybox](http://benno.id.au/blog/2007/11/14/android-busybox "Busybox for android") 用于执行实际挂载。一旦安装完毕，你只需要进入环境，就可以开始使用原生的 Linux 应用程序了。[Jay]通过使用 unionfs 使 Android 和 Debian 环境共享同一个根，更进了一步。这确实是一个很好的方法，并且知道模块可以被添加到内核中也很好。

[照片: [tnkgrl](http://flickr.com/photos/tnkgrl/2963841190/in/set-72157608262752711/)

[via [Hackszine](http://www.hackszine.com/blog/archive/2008/11/installing_debian_alongside_an.html "Installing Debian alongside Android on the G1")