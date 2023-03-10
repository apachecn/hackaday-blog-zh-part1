# 使用 LED 立方体作为音频可视化工具

> 原文：<https://hackaday.com/2011/08/04/using-an-led-cube-as-an-audio-visualizer/>

[![](img/a4cb07c617f59200fd55e443c2787670.png "cube")](http://hackaday.com/wp-content/uploads/2011/08/cube1.png)

[Isaac]发送了他的 LED 立方体与图形情商测量仪的混搭构建。[建造](http://imblackmath.blogspot.com/)相当简单，从[的视频](http://www.youtube.com/watch?v=KGAUCPmDVYE)中我们可以看出，他的建造将是一个在 dubstep 场地中的伟大装置。虽然它不是 9x9x9 的立方体，但通过一些[明智的编码](http://hackaday.com/2011/07/26/update-arduino-shift-register-pwm-gets-speed-boost/)，我们认为这是一个非常适合预期目的的显示器。

与使用电阻和电容网络的纯模拟音频可视化不同， [MSGEQ7](http://www.mix-sig.com/index.php?option=com_content&view=article&id=145%3Amsgeq7-&catid=52&Itemid=127) 是一款 7 频段图形均衡器 ic，基本上不需要支持电路。立方体由几个移位寄存器供电，占用他的 Arduino 上的三个引脚。

即使有了巨大的 LED 立方体，分辨率仍然太低，除了玩贪吃蛇或乒乓球游戏之外，做不了什么。[立体显示器](http://hackaday.com/2010/08/09/spin-peggy-get-3d-pov/)，虽然提供了更高的潜在分辨率，但依靠一种机制来高速旋转显示器。[Issac]的建筑绕过了这一限制，在他的 EQ 的每个波段只需要几个 led。这是一个非常好的构建，为所有的 LED 立方体赋予了一个目的。