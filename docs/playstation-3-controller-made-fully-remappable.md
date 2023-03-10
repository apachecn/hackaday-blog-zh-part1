# PlayStation 3 控制器完全可重新映射

> 原文：<https://hackaday.com/2011/10/11/playstation-3-controller-made-fully-remappable/>

![](img/106f404dcd7eb8e9f9b60c1a5165da13.png "remappable-ps3-controller")

[Hazer]设法取得了一个 PlayStation 3 六轴控制器，并对其进行了修改，以便所有按钮都可以在硬件中重新映射。除了这真的很酷，他还有一个很好的理由这样做。老读者应该还记得关于(查克·比特纳的)互联网请愿书呼吁将[按钮映射作为所有游戏](http://hackaday.com/2010/05/15/button-mapping-for-all/)的一个功能。由于这个行业还没有在这个领域接过火炬，[Hazer]开发了这个 mod 供[Chuck]使用，并且已经发布给任何想尝试一下的人。

硬件改造相当棘手。在图片的左边，就在隆隆电机的下面，一个 DIP 微控制器是死虫风格的。这是一张 PIC 18F14K50。它运行的是引导程序，在控制器的另一侧有自己的 USB 端口。通过切割走线和焊接过孔，该芯片拦截按钮按压，并根据 EEPROM 中存储的替代映射将它们发送到控制器的处理器。有一个助手应用程序，可以让你将控制器插入电脑，指定每个按钮的功能，包括按钮的切换等功能。休息过后，看看[Chuck]对视频中硬件的看法。

[https://www.youtube.com/embed/bV6MaHB1pO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bV6MaHB1pO4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢马特]