# 网络控制的黑暗水晶

> 原文：<https://hackaday.com/2009/09/19/web-controlled-dark-crystal/>

![mood_rock_using_shiftbrights](img/55cf6679dee3f2f5467becdce4d68f5f.png "mood_rock_using_shiftbrights")

[雷扎]送来了他的心情摇滚。与其他“情绪”设备不同，它不是显示你的情绪，而是显示互联网的情绪。两个 [ShiftBrite 模块](http://macetech.com/blog/node/83)由 AVR ATmega8 控制，然后通过 USB 连接到计算机。这个组件被放在一块雪花石膏里面。

USB 通信由运行 [V-USB(以前的 AVR-USB)固件](http://www.obdev.at/products/vusb/index.html)的 ATmega8 控制。[Reza]使用 Perl 和 AJAX 编写了一些代码来控制 web 上的颜色。[前往网络界面](http://rezasf.mine.nu/rock.html)自行设置颜色。如果能添加一个实时网络摄像头，我们会很高兴，这样我们就能在石头上看到我们的心情。 [https://www.youtube.com/embed/aUOcE_a_99c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/aUOcE_a_99c?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)