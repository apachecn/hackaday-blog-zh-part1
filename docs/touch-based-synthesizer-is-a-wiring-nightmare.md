# 基于触摸的合成器是一个布线噩梦

> 原文：<https://hackaday.com/2011/05/11/touch-based-synthesizer-is-a-wiring-nightmare/>

![](img/1101f3dbc96004baf0da588902ec1a37.png "touch-based-sequencer")

[Jane]来信让我们了解她和她的同学刚刚制作的基于触摸的合成器。他们称之为 ToneMatrix Touch，因为它的灵感来自于[一款名为 ToneMatrix](http://lab.andre-michelle.com/tonematrix) 的 flash 应用。我们熟悉这个应用程序，因为它也是其他物理构建的[灵感。](http://hackaday.com/2010/06/30/physical-tone-matrix/)

该设备表面玻璃中的电阻式触摸屏提供了通过点击您希望打开或关闭的电池进行交互的能力。玻璃下面是一个 led 网格，代表循环合成器轨道中的声音位。十五个移位寄存器驱动 LED 矩阵，整个系统由 ATmega644 微控制器控制。虽然控制方案非常直接，但用于将矩阵连接到移位寄存器的跳线构成了隐藏在机箱内的最高级的 wireporn。休息后看看演示视频，看看这是什么样子和使用时的声音。

【维梅奥 http://vimeo.com/23542983 w = 470】