# AVGA:基于 AVR 的视频游戏平台

> 原文：<https://hackaday.com/2009/08/12/avga-the-avr-based-video-game-platform/>

![avrvideogame](img/1bd10d299b01e1e712070b2c8d8e45b8.png "avrvideogame")

我们已经看到了相当多的 AVR 项目，但是这个非常酷。 [AVGA](http://avga.prometheus4.com/) 是一款基于 Atmel AVR 系列微控制器的彩色视频游戏开发平台。如上图所示，该项目使用的 AVR 之一是流行的 ATMega168。使用 AVR 运行彩色视频游戏有几个技术障碍；最困难的问题之一是找出一种方法来显示 AVRs 有限的板载 RAM 中的详细图形。最终，开发人员想出了一种使用基于图块的驱动程序来显示详细图形的方法。图块驱动程序的工作原理是将屏幕划分为 X 和 Y 坐标，将图形划分为图块。然后，当需要图形时，它从存储在 AVR 板载 RAM 中的参考表中寻址，允许位图图形从游戏的 rom 中加载。目前，该平台唯一可用的游戏是超级马里奥克隆版、吃豆人克隆版和蛇克隆版。虽然只有几款游戏可用，但这个平台看起来肯定很有前途。如果有的话，这个项目作为一个伟大的例子，什么现成的微控制器的能力。