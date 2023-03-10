# 小型 POV 设备展示了一些大功能

> 原文：<https://hackaday.com/2011/04/26/small-pov-device-shows-off-some-big-features/>

![](img/12dc9a076262ade03d1b223eb353820f.png "small-pov-with-big-features")

我们已经在下一个零件订单中添加了构建[Rucalgary]的[微型视点设备](http://rucalgary.hackhut.com/2011/04/26/upov-with-better-firmware-pics-video-and-source/)所需的组件。这个小装置为视觉板的微小持久性设立了一个新标准。Rucalgary 使用了一个加速度计，而不是依靠用户来找到摆动板子的最佳速度和时机。由于加速度计的成本，这是我们经常抱怨的地方。我们仍在呻吟，但这次是因为不同的原因。

这里使用的加速度计是飞思卡尔 MMA7660。这是一款 i2c 设备，价格超低，不到 1.50 美元。我们仍然抱怨的原因是，它采用 DFN-10 封装，比 SOIC 更难焊接，但如果你有耐心和良好的铁，这是可以做到的。ATmega48 驱动该设备，带有 8 个 led 和一个输入按钮。在电路板的背面，有一个 CR2032 纽扣电池的支架和一个用于对设备进行编程的母 SIL 引脚接头。

请查看休息后嵌入的视频演示。我们喜欢它的信息拼写和排列正确，无论小黑板是挥舞的方式。

[https://www.youtube.com/embed/FDQs6d8fqks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FDQs6d8fqks?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢保罗]