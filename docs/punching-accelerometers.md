# 冲压加速度计

> 原文：<https://hackaday.com/2010/04/15/punching-accelerometers/>

![](img/9f5bf72e762650f072c3f2e9bedefecf.png "See, there ARE geeks out there who know how to punch! ish...")

[在](http://abieneman.wordpress.com/2010/04/04/punch-acceleration-sensor/)完成他的 [Makiwara 出气筒](http://abieneman.wordpress.com/2010/04/02/diy-wall-mounted-makiwara/)后不久，【阿比尼曼】[连线](http://abieneman.wordpress.com/2010/04/04/punch-acceleration-sensor-%E2%80%93-part-2/)和[编程](http://abieneman.wordpress.com/2010/04/06/punch-acceleration-sensor-part-3/)一个 Arduino 到一个加速度计，以找出他出拳后的加速度(和一些数学，力量)。这个项目很简单，并且可以很快地为你自己的测量和实验重现:他使用的所有东西包括一个 Arduino、[加速度计](http://www.sparkfun.com/commerce/product_info.php?products_id=9332)(带 A/D 转换器)、LED 显示器(和移位寄存器)。当得知加速度计产生了多少静电时，我们有点失望，因此测量诸如冲量、能量和几乎任何非运动学的东西都是无效的。但这让我们想知道，比如说，Wii 遥控器[的出气筒里会有多少静电？](http://hackaday.com/?s=wii+remote)