# 内置 7 段 PS3 显示屏

> 原文：<https://hackaday.com/2011/07/08/internal-7-segment-ps3-display/>

![](img/444a1e328531a44b4060294d9c1ae492.png)

[Zach]发送了他的 PS3 温度控制器和显示器，尽管它只能与 PS3 fat 一起工作，但我们非常喜欢我们的 PS2 向后兼容性，谢谢。

建造开始时[扎克]在他的 PS3 的 CPU、RSX 和北桥上安装了热传感器。在开始用他的笔记本电脑控制风扇后，在看到这个关于“隐藏显示器”的[帖子](http://www.ps3hax.net/showthread.php?t=23616)后，他转向了集成风扇和显示器控制器最终，一个我们见过的最酷的 PS3 mods 诞生了。

该构建运行 Arduino Pro，它从传感器获取温度，将一切打印到自定义的 7 段显示板上，并控制风扇。[Zach]谢天谢地，我们提供了 Arduino 源代码，如果你想自己制作的话，我们还提供了一些电路板文件。这是一个非常令人印象深刻的构建，当 PS3 关闭时完全看不见。

风扇控制器的设计过程非常有趣。它最初是由 4 个独立的 2 位数显示屏组成的，后来发展到由 5 个 LED 指示灯组成的 [2 显示屏。七个 7 段显示器](http://www.youtube.com/watch?v=x4AZgYFpuJI)[和一个非常整洁的定制板](http://killerbug.net/IMG/KB_PS3_HWMOD_PCB_MCP23008s_InstalledBack_BIG.jpg)被用在最终的构建中。

这些显示板的 Gerber 文件可以下载，对其他项目肯定有用。查看风扇控制器的视频，并在下面进行展示。

[https://www.youtube.com/embed/ynWb8_MXAEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ynWb8_MXAEM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)