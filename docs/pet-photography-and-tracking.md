# 宠物摄影和跟踪

> 原文：<https://hackaday.com/2008/07/09/pet-photography-and-tracking/>

我们已经看到了许多旨在跟踪您宠物的位置和活动的产品，上个月就有两款，但我们确信您可以制造出比您所能购买的更多的功能设备。让我们看看几个，并考虑我们的选择。

![](img/978374a85c9ed1011e85aaae589ba4dc.png)
一台名为[宠物视角](http://www.entertainmentearth.com/prodinfo.asp?number=UM1538)的相机挂在你宠物的项圈上，按照你选择的 1 分钟、5 分钟和 15 分钟间隔拍摄照片。虽然这个概念很好，但执行却很差:它最多只能拍摄 35 张 640 x 480px 的图像，没有其他分辨率选项，而且它没有可扩展的媒体插槽。我们也不喜欢缺乏 GPS 跟踪，但不会真的期望为 45 美元的价格。

![](img/459b2ef0bcf20b2958f1e438579d1844.png)

对于 GPS 宠物跟踪，Garmin 最近推出了他们的 Astro 系统，该系统由一个带 GPS 的[项圈和一个跟踪单元](https://buy.garmin.com/shop/shop.do?pID=8576#)组成。像大多数 Garmin GPS 产品一样，这款产品功能齐全，功能和技术完美结合。我们喜欢实时跟踪宠物的位置，但我们没有 600 美元来跟踪狗。

与两个商业解决方案相比，一个我们更喜欢的自制解决方案是[[j . Perthold]的 cat cam](http://www.mr-lee-catcam.de/index.htm)。从一个 20 美元的 130 万像素分辨率和 SD 卡插槽的钥匙链相机开始，[Perthold]拆除了外壳，并将电路板连接到 Attiny2313 微控制器，该微控制器被编程为定期触发相机。他为他的改装相机做了一个小而轻的箱子，并把它绑在他的猫(李先生)身上。这实际上是与宠物的视野相机一样的产品，但是几乎每一个适用的标准都至少是两倍。

我们喜欢 CatCam 的一点是它使用 SD 媒体。如果你使用一个[目镜](http://www.hackaday.com/2008/06/27/eye-fi-explore-review/)而不是普通的媒介，你就可以拥有一个比宠物的目镜更好的相机，并且可以在一个包中完成地理标记。它没有真正的实时 GPS 有用，但至少当你收集照片时，你会知道你的宠物去了哪里。此外，如果狗仍然在您的家庭网络范围内，您应该能够看到图像流。如果构建一个支持 Eye-Fi 的 CatCam 太麻烦，可以考虑在佳能相机中使用带有 [CHDK](http://www.hackaday.com/2008/05/27/how-to-expand-your-camera-with-chdk/) 的 Eye-Fi。这将为您提供一个易于构建的包中的定时摄影和地理标记。希望你选择一个小相机，除非你的宠物有一个强壮的脖子。你可以使用我们之前发布的一些[延时摄影](http://www.hackaday.com/2008/07/09/intervalometers-and-timelapse-photography/)技术来为你最终使用的任何设备计时。

*   [永久链接](http://www.mr-lee-catcam.de/index.htm)