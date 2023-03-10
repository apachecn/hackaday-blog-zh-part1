# 初学者概念:595 移位寄存器模拟器

> 原文：<https://hackaday.com/2011/03/14/beginner-concepts-595-shift-register-simulator/>

![](img/091849c751bcf3a8bb8a8979ae7de8dd.png "595-shift-register-simulator")

[Aaron]刚刚完成构建一个在线 595 移位寄存器模拟器。这些廉价的芯片可以让你扩展单个微控制器可以控制的设备数量。你可以在很多 LED 复用项目中看到它们，包括我们最近建造的[乒乓时钟](http://hackaday.com/2011/01/31/how-to-build-a-ping-pong-ball-display/)。但是如果你不熟悉硬件的话，要完全掌握它们可能有点困难。

该模拟器为 595 移位寄存器上的五条可能的控制线提供了一个点击式界面。使用该装置必须操作三个销；串行输入、时钟和锁存引脚。另外两个用于清除寄存器和使能输出，可以认为是可选的。您可以选择在自己的项目中使用微控制器来控制这些功能，以获得更大的灵活性，但当这些功能不必要时，它们通常会连接到 VCC 或 GND(取决于芯片)。试试这个模拟器，然后把你学到的东西带到无焊试验板上，看看你是否能写一些固件来产生同样的结果。如果你仍然有问题，你可以看一下这个 595 教程以获得更多信息。