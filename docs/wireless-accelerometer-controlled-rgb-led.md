# 无线加速度计控制的 RGB LED

> 原文：<https://hackaday.com/2008/10/09/wireless-accelerometer-controlled-rgb-led/>

![](img/1ff72cc44d6bc9b627208de3c8425bc8.png "wireless_led")

给了我们这个很酷的小项目。他建造了一个由无线加速度计控制的 RGB LED 照明系统。基于满嘴的食物，听起来很复杂，对吧？最终结果看起来相当直观。只需拿起控制器，倾斜你的手来改变灯光的颜色。

控制器由 Atmel AVR168 微控制器组成。他没有具体说明他使用的是什么收发器，但如果你在评论中看到，他指出他添加了一个天线来扩大范围。控制 LED 的部分基于 Atmel AVR169 微控制器，该微控制器与一些 [shiftbright LED](http://hackaday.com/2008/05/08/maker-faire-2008-shiftbright-rgb-led-module/) 模块相连。

它的射程在 20 米左右。颜色之间的过渡非常平滑，你可以在下面的视频中看到。

[https://www.youtube.com/embed/M07UJUg7yZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/M07UJUg7yZo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)