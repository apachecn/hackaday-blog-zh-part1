# 用遥控控制器玩 SNES

> 原文：<https://hackaday.com/2011/08/14/playing-snes-with-an-rc-controller/>

[![](img/6d399be24b8a4b83b087ce4f5fe0061f.png "fubata")](http://hackaday.com/wp-content/uploads/2011/08/fubata.png)

通常情况下，当我们看到 R/C 发射器用于建造时，我们会想到机器人、四轴飞行器或无人机。[Alex]为他的双叶收音机找到了一个新用途—[把它连接到他的超级任天堂](http://brainlubeonline.com/Futaba2SNES/RC_SNES%21.html)上。

我们已经看到很多构建使用游戏控制器作为其他硬件的接口。我想到了 N64 媒体遥控器 T1，还有 T2 的 NES iPod 音乐基座 T3。除了[自动为你赢得游戏内货币](http://hackaday.com/2011/02/02/automating-automatic-racing/)的几个版本之外，我们还没有看到多少用附加电子设备来控制视频游戏的东西。[Alex]的建造很高兴地抵制了这种趋势，并且*在技术上*给了 SNES 一个模拟控制器。

该构建使用一个 [mBed 微控制器](http://mbed.org/)来捕获收音机的按钮和操纵杆位置。这通过两个移位寄存器发送，以产生 SNES 控制器协议所需的 16 位数据包。[Alex]为他的构建发布了所有的[软件](http://brainlubeonline.com/Futaba2SNES/CODE.html)，从它的外观来看，代码似乎相当可移植。[亚历克斯]说他正在让他的世嘉土星和他的双叶跑起来，所以我们迫不及待地想看到一些*装甲龙骑兵*的行动。休息之后，看看[Alex]用 Gradius III 演示他的控制器。

[https://www.youtube.com/embed/uMvOR4fW50Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uMvOR4fW50Q?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)