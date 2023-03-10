# 用于廉价蓝牙模块的固件编程器

> 原文：<https://hackaday.com/2012/01/30/firmware-programmer-for-a-cheap-bluetooth-module/>

这里有一个廉价蓝牙模块的漂亮程序员。这部分到底有多便宜？[6.60 美元听起来像是一笔极端的交易吗](http://dx.com/wireless-bluetooth-rs232-ttl-transceiver-module-80711)？

关于这次攻击的信息在[的一系列帖子](http://byron76.blogspot.com/search/label/HC05)中传播。上面的链接指向完整的程序员(有点像对黑客的回顾)。但是你可以从[这篇关于模块固件选项](http://byron76.blogspot.com/search/label/HC05)的文章开始。仅仅因为你能便宜地得到这个零件并不意味着它会像你预期的那样工作。[Byron]从不同供应商处采购类似设备，发现它们运行的固件不同；脚印是一样的，但他的特征不一样。在他的帮助下，你可以根据自己的需要修改代码并刷新设备。

他构建的编程器有一个很好的模块插槽，可以使用弹簧针(弹簧触点)与编程线连接。它连接到 CSR BC417 芯片的 SPI 引脚，以便刷新固件。如果你有使用这些廉价零件的经验，我们很乐意在评论区听到你的故事。

[感谢 MS3FGX]