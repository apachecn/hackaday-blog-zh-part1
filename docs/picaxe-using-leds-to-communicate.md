# PICAXE 使用 led 进行通信

> 原文：<https://hackaday.com/2011/03/15/picaxe-using-leds-to-communicate/>

![](img/aa70ba5d1c6162f53ad0b8f4e6dffc15.png "LEDs-for-wireless-communication")

[Relwin]一直在研究使用 led 作为双向设备的。上面的设置允许他使用每个 LED 作为输入，寻找明亮的光源，然后与它接收的活动同步。这是使用组件的最基本的通信。系统的核心硬件是左边的 PICAXE 开发板。右边的闪烁光会导致图片左边的 LED 闪烁，但是将闪烁源移到那一边会反转效果。该芯片被编程为每当失去连接时就在压电蜂鸣器上播放一首曲子。我们感兴趣的是，这些绿色 LED 不会检测到红色 LED 闪烁，因为检测器端的电压阈值不同。

他有一些可用的代码，但我们真的在寻找如何处理这个概念的想法。也许是类似于 [LED 矩阵视频拼图](http://hackaday.com/2010/07/02/great-interactive-led-puzzle/)的东西，或者是[这款激光笔 LED 游戏](http://hackaday.com/2010/05/04/laser-command-game-uses-laser-for-control/)的变体。休息后观看演示视频，然后留下评论让我们知道你会用它做什么。

[https://www.youtube.com/embed/sXNebej_zlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sXNebej_zlg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)