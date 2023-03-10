# 将扫描仪转换为触摸屏

> 原文：<https://hackaday.com/2011/03/21/converting-a-scanner-into-a-touchscreen/>

![](img/fcb4db8789d43b64bfd86f0a584c85db.png "scanner-multitouch-display")

[Sprite_TM]在清理他的黑客工作台时，他发现了一台曾经风光一时的一体机。经过一番考虑后，他决定拆除设备的扫描仪部分，最终[将它变成一个多点触摸显示屏](http://spritesmods.com/?art=lineccdts)。

扫描仪依赖于一个长 PCB 和一个线阵 CCD 传感器。该传感器的读取方式类似于信息沿移位寄存器传递。告诉它读取一个读数，然后启动一个时钟信号，从传感器的像素中脉冲输出每个模拟值。为了扫描彩色图像，它使用多色发光二极管在不同的照明下读取不同的读数。

[Sprite_TM]利用这一功能将其转变为多点触摸传感器。传感器板本身安装在 LCD 显示器下方，并带有一个带狭缝的护罩，以帮助过滤环境光。在屏幕上方，一系列发光二极管照射在传感器上。当你用手指打断光束时，它会投射出一系列的阴影，这些阴影被传感器拾取并在软件中处理。休息后观看剪辑，亲自观看。它没有问题检测和跟踪多个接触点。

[https://www.youtube.com/embed/Avb23FWcEeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Avb23FWcEeU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)