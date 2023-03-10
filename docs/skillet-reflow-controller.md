# 滑板回流控制器

> 原文：<https://hackaday.com/2010/12/09/skillet-reflow-controller/>

![](img/bc376f33509bcd1370aae6ae1d52ff1f.png "skillet-reflow")

使用电锅来回流焊表面贴装电路板是这些厨房电器的一种流行的替代用途。真正的诀窍是监测和控制温度。[Mechatronics Guy] [用热敏电阻、固态继电器和 Arduino 构建了自己的煎锅温度控制器](http://sites.google.com/site/mechatronicsguy/reflow-skillet)。

他受到了[lady ada]的工作的启发，该工作使用伺服系统来调节煎锅电源上的温度旋钮。首先使用 JB 焊接将热敏电阻连接到煎锅的底部。由于该区域会变热，他还安装了一个接线盒，用于连接馈线，因为热量会熔化任何焊点。这些电线回到装有 Arduino 和固态继电器的控制箱。为了更好地控制加热元件，继电器被打开和关闭，从而产生低频脉宽调制，这应该有助于保持稳定的温度，而不仅仅是转动电线上的温度旋钮。

将它与真空镊子配对，你就可以走上表面贴装生产线了。如果你想看这个过程的运行[，看看这个帖子](http://hackaday.com/2009/10/13/how-to-populate-a-surface-mount-pcb/)。它从模板印刷，到填充，再到在烤箱里回流。

[谢谢罗伯]