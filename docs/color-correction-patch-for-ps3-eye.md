# PS3 眼用色彩校正贴片

> 原文：<https://hackaday.com/2009/11/09/color-correction-patch-for-ps3-eye/>

![ps3-eye-color-correction](img/b2e267782fa47711fd2d34e6d4bcaa0d.png "ps3-eye-color-correction")

[Max]很高兴看到 PlayStation 3 Eye 在较新的 Linux 内核中得到支持。在他的壁橱里放了一段时间后，这将给相机另一个有用的机会。不幸的是，驱动程序不包括帧率选择和颜色校正，所以他开始写[一个补丁来控制颜色设置](http://bear24rw.blogspot.com/2009/11/ps3-eye-driver-patch.html)。正如你在上面看到的，他的成功极大地提高了你从设备上获得的图像质量。

我们感觉索尼游戏设备的相机外设似乎是一个好主意，但作为一个现实的游戏界面没有太多的持久力。有了像[马克斯]这样的贡献，它们可以被重新利用。PS2 有自己的 EyeToy，它长期以来一直享有对 Linux 的驱动支持。NUI 小组在多点触控方面做了很多工作，并推荐 [PS3 Eye 用于他们的项目](http://hackaday.com/2008/11/28/tbeta-cross-platform-multitouch/)，因为它们价格便宜，帧速率高，图像质量不错。

干得好[Max]。看起来他已经把这个补丁上传到了内核的摄像头模块中。