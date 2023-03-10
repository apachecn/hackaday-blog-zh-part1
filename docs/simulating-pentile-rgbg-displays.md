# 模拟 PenTile RGBG 显示器

> 原文：<https://hackaday.com/2011/12/09/simulating-pentile-rgbg-displays/>

![](img/6c9d0e6523d609e7ca7c000903275c59.png "pentile-screen-simulator")

这里有一个有趣的实验，让你在普通的液晶显示器上模拟 PenTile 显示器。[Barrett Blackwood]想要测试一些图形在不同像素密度的 PenTile RGBG 显示器上的显示效果。这些 [PenTile RGBG](http://en.wikipedia.org/wiki/PenTile_matrix_family) 矩阵有时用于有机发光二极管显示器。例如，Nexus One 智能手机就采用了这种显示屏。因为红色、绿色和蓝色 OLEDs 发出不同强度的光，为了平衡颜色混合，像素的布局与 LCD 面板不同。我们的眼睛能很好地看到绿光，因此绿色子像素比红色和蓝色子像素小得多。

由于硬件布局不同，当在 PenTile 显示器上查看时，一些图形看起来有交叉阴影。[Barrett]制作了上面的例子来模拟图形在传统 LCD 屏幕上的外观(左图)，以及它们在 PenTile 屏幕上的外观(右图)。上面看到的洋红色色调是调整图像大小的结果。由于模拟方法关闭了图像中 1/3 的绿色像素，调整其大小会破坏仔细的计算。必须以 1:1 的比例观看才能正确地看到图像，此时洋红色会神奇地消失。