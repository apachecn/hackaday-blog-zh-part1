# CNC 硬件:将 g 代码流传输到 Arduino

> 原文：<https://hackaday.com/2010/07/21/cnc-hardware-stream-g-code-to-an-arduino/>

![](img/7df5f029f903b1c40a1e7284bf008743.png "arduino-cnc-gcode-receiver")

[礼萨·马奈]使用 Arduino 作为他的 CNC 设置中心已经有一段时间了。它处理三个步进电机、限位开关、紧急停止和主轴控制。他正在使用的草图允许他将 g 代码流式传输到流行的原型平台，使他不再需要专用的 PC。这种方法非常有效，以至于他决定清理代码，开发一个盾牌来帮助其他人开始运行。如果你想看看他的进步或者帮他一把，可以查看一下他创建的 google group 的图表、代码和论坛讨论。已经有[一个 Arduino 的 CNC 项目叫做 Grbl](http://grbl.tumblr.com/) ，但是【Reza 的】方法使用 Arduino 库，努力使草图对普通用户来说更加可定制。