# 1.5 英寸相框的逆向工程

> 原文：<https://hackaday.com/2012/01/31/reverse-engineering-a-1-5-inch-photoframe/>

![](img/37b25e5723e2c487d241918aefbf6d3d.png "Untitled")

小小的，没有名字的，1.5 英寸液晶照片钥匙链到处都是，几乎没有。不足为奇的是，这些东西在它们使用的部件上没有太大变化，一些闪存 ram，一点 lipo 电池和一个 16 位彩色 LCD。想要找到一种重新使用 LCD 的方法[Simon]有一个很好的教程，教你如何在你的电子项目中使用带有 ILITEK ILI9163 LCD 驱动程序的 FTM144D01N LCD。

使用了两个单元，一个被拆开并焊接到一个自制的分线板上，另一个保持完整，这样就可以用示波器嗅出它的逻辑。由于这些设备通常使用 8 位或 16 位数据总线，因此可以快速确定引脚排列。然后为 AVR 微控制器编写了一个驱动程序库，包括一些基本的图形和一个 5×8 的字体。

虽然你可能没有足够的运气从你当地的廉价商店买到这种液晶显示屏，但这里有很多提示，希望能让你行动起来。今天下午我们将在一个非常相似的屏幕上试试运气，因为这些东西确实有一个不错的图片和相当快的响应时间，已经包装在一个手持的盒子里。

休息之后，请加入我们，观看一段简短的视频。

[https://www.youtube.com/embed/uLn1Oz2wCJ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/uLn1Oz2wCJ8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)