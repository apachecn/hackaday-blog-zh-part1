# 重建布里奇波特工厂

> 原文：<https://hackaday.com/2011/11/13/rebuilding-a-bridgeport-mill/>

看起来互联网的常驻蒸汽锅正在上升一两个世纪。[Jake Von Slatt] [重建了 Bridgeport 系列 II 轧机的 CNC 部分](http://steampunkworkshop.com/bridgeport-series-ii-cnc-geckomach3-conversion),使其可以与计算机连接。这一壮举甚至比[将磨坊](http://steampunkworkshop.com/moving-bridgeport-milling-machine-recreational-rigging)搬进【杰克】的车库更令人印象深刻。

构建的第一步是拆除 BOSS 5 工业微型计算机，代之以运行 ArtSoft Mach 3 的 Win XP 笔记本电脑。这允许 g 代码直接显示在屏幕上。工厂的旧电源确实给[杰克]带来了一些问题。取代旧电子设备的[壁虎步进驱动器](http://www.geckodrive.com/g203v-p-34.html)无法处理旧电源的电压。这可以通过[打开变压器](http://steampunkworkshop.com/sites/default/filimg/Bridgeport-Series-II-Conversion05.JPG)并移除几圈电线来解决。

[杰克]最近已经发了一些他的黑客作品，所以很高兴看到《黑客一天》又有了一个粉丝，尤其是像[冯·斯莱特先生]这样有才华的人。但是磨坊改造有一个问题——[杰克]还没想出如何编程。如果有任何 HaD 读者想就工厂 g 代码编程的最佳方式发表意见，请随时在评论中留言。