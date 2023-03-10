# USB 主机来到 Zipit

> 原文：<https://hackaday.com/2010/09/18/usb-host-comes-to-zipit/>

![](img/963f80e7607476973cf33aeb7d5551e5.png "zipit-usb-host-module")

这种 USB 到 Zipit 的坞站适配器和特殊的内核使 Zipit 的 [USB 主机模式成为可能](http://www.mozzwald.com/node/60)。以前，这种便宜且可破解的无线客户端需要修改硬件才能支持 USB。名为 [U-Boot](http://www.mozzwald.com/node/59) 的新内核引导程序使得内部改动变得不必要(休息后请看演示)。现在唯一需要注意的是电压问题。当使用电池运行时，Zipit 仅提供 3.3V 电源，因此您可以选择仅在 Zipit 插入充电器时使用 USB，或者使用带电源的 USB 集线器。但是，如果你已经在构建一个集线器适配器，添加电池供电的集线器应该不会太麻烦。

那么我们现在可以用 USB 控制器[玩我们的 NES 游戏](http://hackaday.com/2010/06/30/nes-controller-to-usb-gamepad/)了吗？

[https://www.youtube.com/embed/Mex0PWkDOoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mex0PWkDOoI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢乔迪]