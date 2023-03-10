# 帕皮杜在看着你！

> 原文：<https://hackaday.com/2011/04/26/papydoo-is-watching-you/>

[![](img/54cc71baf56e3fc69b530188b4b0327b.png "Papydoo (Custom)")](http://hackaday.com/2011/04/26/papydoo-is-watching-you/papydoo-custom/)

Papydoo 大部分时间都在睡觉，但如果受到震动的惊吓，它就会醒来，用一种你从未见过的冰冷和令人不安的机械目光盯着你。或者，它可能只是做一些疯狂的事情，如显示一个滚动的空间入侵者字符字幕。帕皮杜就是这样，你永远不知道。

振动感测是通过一个压电元件实现的，这个压电元件是从一个旧的喇叭扬声器中获取的，简单地夹在项目外壳和它所在的表面之间。MCP601 运算放大器用于放大来自压电元件的微弱电位，并将其馈入 Zilog Z8F083A 微控制器的 ADC。当检测到足够的振动时，MCU 唤醒，并在前面板 32X8 LED 矩阵上显示多种不同动画中的一种。也可以使用外壳背面的小按钮手动选择各种显示模式。

休眠时功耗降至 150uA，只需每秒短暂唤醒 MCU 一次，以检查当前振动水平。几乎所有这些功耗都可以归因于运算放大器，虽然有更高效的型号可用，但有时最佳选择只是您手头上的一个器件。无论如何，它的功耗足够低，可以用一组 AA 电池供电。

我们可以想象，类似的设置可以用于许多不同的低功率消息应用程序，这些应用程序只有在有人足够接近以进行阅读和交互时才会“醒来”。添加一个扬声器，这甚至可能成为一个很好的警报，让讨厌的同事远离你的“立方体”。你会用纸做什么？

谢谢你的提示[劳伦斯]！如果你碰巧读到这封信，我们很想知道:为什么是“Papydoo”？

休息后的短视频。

[https://www.youtube.com/embed/Q-b-v5Yo_hw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Q-b-v5Yo_hw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)