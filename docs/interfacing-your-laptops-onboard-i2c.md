# 与笔记本电脑板载 I2c 接口

> 原文：<https://hackaday.com/2008/05/14/interfacing-your-laptops-onboard-i2c/>

![](img/1b131d66d6addf5731ba8f9fd888e7e0.png)
【lady ada】[偶遇](http://www.ladyada.net/rant/2008/05/microcontroller-less-i2c-adapter/) [这位](http://www.paintyourdragon.com/uc/i2c/index.html)出色的黑客被【菲利普】。显然，在大多数现代视频连接中都有时钟、数据、5v 和接地连接。(他甚至注意到了 HDMI 电缆引脚)他编写了一些驱动程序，现在可以直接从 ~~PC~~ Mac 控制 i2c 硬件。[Ladyada]指出，大多数笔记本电脑也使用 i2c 总线来连接额外的传感器。目前，[代码](http://members.dslextreme.com/users/paintyourdragon/uc/i2c/i2c.tar.gz)只适用于 Mac OS X。