# PWM 控制的 led 显示屏是真正发自内心的礼物

> 原文：<https://hackaday.com/2011/03/16/pwm-controlled-led-display-is-truly-a-gift-from-the-heart/>

![led_heart_panel](img/3ba2f0773f6f05ab9707956861451dcf.png "led_heart_panel")

Instructables 用户[Simon]承认他对电子产品上瘾。对他来说幸运的是，他 15 年的妻子对他摆弄任何插电设备的需求相当冷静，或者至少是容忍的。作为他们结婚周年纪念的礼物，他决定将他对妻子的爱与他对电子产品的爱结合起来。结果就是你上面看到的 [RGB LED“爱心”](http://www.instructables.com/id/RGB-LED-Love-Heart)。他建立了一个由 PIC12F683 微控制器控制的 RGB LED 电路，该电路照射到手蚀刻的有机玻璃面板上。

正如您所料，LED 颜色是通过 PWM 控制的。然而，你可能没有预料到的是[Simon]为了确保他在项目中使用的 5 个 led 的颜色和亮度几乎完美匹配而走的路。由于 RGB LEDs 没有统一的输出亮度，他使用了勒克斯计来精确测量每个 LED 的白平衡。然后，在对 PWM 驱动器进行编码之前，他在 Excel 中绘制了结果。这才是虔诚！一旦 led 安装完毕，他就着手建造 LED 面板的其余部分。

如果你有兴趣为你的心上人建造一个，那么[Simon]会为你提供完成这项工作所需的所有原理图、模板和源代码。

请继续阅读，观看他的心脏小组活动视频。

[https://www.youtube.com/embed/bgqvyfl-Fv4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/bgqvyfl-Fv4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)