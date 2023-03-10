# 从 FPGA 板构建的 CRT 矢量图形街机游戏

> 原文：<https://hackaday.com/2012/03/16/crt-vector-graphics-arcade-game-built-from-an-fpga-board/>

![](img/491fad045e198177058726614ac8da56.png "fpga-based-vector-CRT-arcade")

[Sprite_TM]想要挑战他的 VHDL 技能，没有比在完成后制作一些可播放的东西更令人满意的方式了。他决定尝试在[创造一个基于向量的 CRT 街机](http://spritesmods.com/?art=bwidow_fpga&amp;f=had)。这里的区别在于，基于矢量的游戏控制着磁环，磁环将电子路径导向屏幕。这种技术允许点对点图形生成，而不是 CRT 电视使用的基于像素的扫描。

他手头有一台小型彩色阴极射线管，决定从网上下载一个 VHDL 版本的小行星，看看能否让它工作。但在进一步检查源代码后，他发现其中有一大块代码将矢量栅格化以供扫描监视器使用。在移除了那一大块，并给它一个旋转之后，他有了足够的信心，他知道他在做什么来开始实现他自己的游戏。选择什么标题实际上取决于最初的街机机柜使用的硬件。他对为《星球大战》和《暴风雨》等游戏中使用的数学芯片实现软过程不感兴趣。最后，他制作了一个版本的黑寡妇，甚至还为它做了一个微型橱柜。休息之后，看看视频中的一些游戏。

[https://www.youtube.com/embed/CroIdhD3veE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/CroIdhD3veE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)