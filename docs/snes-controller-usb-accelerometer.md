# SNES 控制器+ USB +加速度计

> 原文：<https://hackaday.com/2010/04/09/snes-controller-usb-accelerometer/>

![](img/9227ae178d1452732a975ee451c91787.png "TeensySNES_Finished-large")

当我们发布关于[Atarity]的[XBMC 藏在一个 SNES 控制器](http://hackaday.com/2010/03/23/xbmc-hiding-in-an-snes-controller/)里的时候，我们正在完成[Adafruit]的[教程](http://www.adafruit.com/blog/2010/04/09/how-to-make-a-usb-game-pad-with-tilt-accelerometer-mouse/)的工作。该教程结合了一个 [Teensy](http://pjrc.com/teensy/index.html) USB 开发板和一个 SNES 控制器内的 3D 加速度计。Teensy 被编程为轮询 SNES 控制器按钮并读取加速度计值。按钮被设置为按键和鼠标按钮，加速度计值被处理为鼠标移动。编程播放[门户](http://orange.half-life2.com/portal.html)，我们制作了一个视频展示如何使用该设备。休息过后你就能看到了。

这不像典型的电脑游戏玩家左手:WASD，右手:鼠标站姿那样简单快捷。然而，我们可以想到一些其他的游戏可以通过使用一种设备来改进，这种设备经过一点黑客攻击，可以根据用户的需要来定时击键。只要再进行一点黑客攻击，这种设备就能破解密码。你还会用这个做什么？