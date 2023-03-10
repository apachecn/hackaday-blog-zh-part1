# 使用 SPI 的模块化系统

> 原文：<https://hackaday.com/2009/12/22/modular-systems-using-spi/>

![](img/54e54a08da221867ab8a087afb9ec8b7.png "modular-led-marquee")

[Humberto]通过 NerdKits 视频再次展示了如何使用 SPI 总线在微控制器之间进行通信。他从之前的 LED marquee 项目开始，该项目仅限于 5×24 LED 矩阵，并开发了模块化解决方案来增加尺寸限制。

休息后嵌入的文章和视频很好地详细说明了独立系统和模块化系统之间的重要差异。好消息是，所用的 ATmega168 芯片内置了基于中断的 SPI 协议。一旦连线正确，主控芯片将分别寻址每个模块，将数据添加到它们的缓冲器中，直到传输完一个完整的帧，然后移动到下一个模块。

讨论了该系统的一些注意事项，如长距离数字传输。如果所有的 LED 都同时点亮，我们会对功率限制产生疑问。但是除了这一点，如果你想玩 LED 显示屏，不要忘记 500 或 1000 个 LED 的订单通常会有巨大的价格折扣！

[https://www.youtube.com/embed/FvsXcpM2qA4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FvsXcpM2qA4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)