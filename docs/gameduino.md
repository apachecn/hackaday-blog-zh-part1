# 甘梅杜伊诺

> 原文：<https://hackaday.com/2011/03/02/gameduino/>

![](img/48fc23df5097b2fda63a93b3f61df3a2.png "game")

Gameduino 是一款基于 FPGA 的[声音和图形适配器](http://excamera.com/sphinx/gameduino/index.html#gameduino)，用于微控制器。作为一个 Arduino 盾牌，它真正需要的是一个带 SPI 的微控制器和一些代码来发送命令到电路板，让您切换寄存器，处理内存和绘图功能。

一旦数据到达那里，它就会受到一个 Xilinx FPGA 的欢迎，该 FPGA 会输出一个 800×600 72Hz 的 SVGA 同步信号、大型 512×512 像素字符滚动背景、一堆 16×16(多达 256 种颜色)子画面，每个子画面都具有每像素透明度、旋转、翻转功能，如果这还不够的话，还有一个 12 位频率的合成器，可以发出 16 种独立的声音。

制作其中一个的所有资源都列在网站上的[制作游戏 id ino](http://excamera.com/sphinx/gameduino/making.html)链接下，但是如果你有兴趣得到一个制作板，也有一个 [kickstarter 页面可用](http://www.kickstarter.com/projects/2084212109/gameduino-an-arduino-game-adapter)。还有其他方法可以从微控制器中挤出视频，从基本的像 [hackvision](http://hackaday.com/?s=hackvision) 到 [AVGA](http://avga.prometheus4.com/) 甚至是 Lucidscience [AVR VGA v2、](http://hackaday.com/2010/11/23/vga-interfacing-avr-microcontrollers/)和大量的 propeller 项目，但这一个是独立的和便携的，有一定的吸引力。

休息之后，请加入我们，观看一段简短的视频。

[https://www.youtube.com/embed/EWn-6FB4cNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/EWn-6FB4cNQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)