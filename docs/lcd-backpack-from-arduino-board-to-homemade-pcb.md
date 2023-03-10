# 液晶背包:从 Arduino 板到自制 Pcb

> 原文：<https://hackaday.com/2011/10/17/lcd-backpack-from-arduino-board-to-homemade-pcb/>

![](img/ed25f4415db248461cfb5fe93d3f8e81.png "SAMSUNG")

[Kaushlesh Chandel]在他的 Arduino 上制作了几个使用 HD44780 字符 LCD 的项目原型。想要保持这些项目的完整性，但不牺牲他的 Arduino 板，所以[他蚀刻了他自己的兼容 Arduino 的 LCD 背包](http://kaushleshchandel.blogspot.com/2011/10/easy-protyping-with-arduino.html)。如果你从来没有通过 Arduino 板来构建一个只使用项目所需部件的模块，这是一个很好的灵感来源，让你尝试一下。

[Kaushlesh]起草的设计非常简单。它直接连接到字符 LCD 的单个内嵌标题。看起来他正在使用 4 位模式来寻址显示器，这给你留下了相当多的引脚(数字和模拟)以供将来使用。他的设计中包含的重要组件是芯片本身、ATmega8/168/328、确保其以正确速度运行以实现 Arduino 计时的晶体，以及用于调整显示器对比度的 trimpot。您希望在自己的设计中包含的最后一项功能是引脚接头，用于通过 FTDI 电缆对芯片进行编程。

以前没蚀刻过自己的 PCB？给[我们的 PCB fab 教程](http://hackaday.com/2008/07/28/how-to-etch-a-single-sided-pcb/)一个尝试。