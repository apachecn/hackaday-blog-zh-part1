# 光学隔离并行端口 I2C 适配器

> 原文：<https://hackaday.com/2006/07/07/optically-isolated-parallel-port-i2c-adapter/>

![parport i2c](img/91f2ff23c9380b91fced4e1c3256ad9c.png)

I2C 是一种类似于单总线的简单通信总线，我们在前面已经讨论过。[hnch]建立了一个真正的[简单的 I2C 并口接口](http://home.arcor.de/henning.paul/i2c_parport.html)。它是光学隔离的，所以你不必担心误炸你的电脑。I2C 模块已经随 Linux 内核一起提供了。它甚至会像处理主板上的温度传感器一样处理你连接的温度传感器，这样你就可以使用 gkrellm 这样的普通软件来监控它们。还有许多其他设备也使用 I2C。[hnch]有一个[神经画廊](http://home.arcor.de/henning.paul/index.en.html)，他会很乐意写下你想要的任何其他项目的信息。

*   [永久链接](http://home.arcor.de/henning.paul/i2c_parport.html)