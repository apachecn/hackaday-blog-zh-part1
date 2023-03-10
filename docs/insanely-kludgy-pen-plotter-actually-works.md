# 疯狂组装笔绘图仪实际工作

> 原文：<https://hackaday.com/2011/10/31/insanely-kludgy-pen-plotter-actually-works/>

![](img/9dd41fbff45cd4369e9726e8afd14ade.png "plot")

这个笔式绘图仪由结构环氧树脂组装而成，是一件令人惊叹的工程作品，几乎和完全由邦多建造的桥梁一样令人印象深刻。

[Brian]在 Rochester，NY hackerspace [Interlock](http://interlockroc.org/about/) 需要为[BarCamp](http://barcamproc.org/)geek“un conference”建造一些东西为了吸引 BarCamp 的参与者来到互锁桌前，他们需要一个带有呼呼马达的小型桌面设备，能够制作一些像样的赃物。组装一个笔式绘图仪听起来是个完美的项目。

构建的机制是从旧的打印机和扫描仪中清理出来的。[Brian]决定使用针式进纸卡片纸，因此旧点阵打印机的卷取轮也牺牲了。该进纸机构用作 Y 轴，X 轴位于精密杆上的纸张上方。笔杆由一个[微型螺线管](https://www.adafruit.com/products/412)支撑。

软件层面的事情开始变得疯狂。 [grbl](https://github.com/simen/grbl) 被加载到一个带有步进驱动器屏蔽的 Arduino 上，并打印出矢量文本图纸。经过一段时间的真人表演后，[Brian]想出了如何绘制捕捉到的网络摄像头图像。OpenCV 捕获并绘制跟踪轮廓。这通过 autotrace 转换成矢量，通过 [pstoedit](http://www.pstoedit.net/) 从 EPS 转换成 HPGL。然后，Python 脚本清理 HPGL，将其转换为 g 代码，并发送到打印机。迷茫？我们也是，所以休息后看看绘图仪的视频。