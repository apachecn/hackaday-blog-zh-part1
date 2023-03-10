# 被黑掉的 LED 圣诞灯

> 原文：<https://hackaday.com/2010/12/01/hacked-led-christmas-lights/>

![](img/f210a38882c9d66e42ff7e836bf7100f.png "Hacked_LED_Xmas_Lights")

[罗伯特]想要从他的 GE 彩色特效 G-35 LED 圣诞灯中得到更多。他逆向工程，然后破解了灯用来交流的协议，这样他就可以控制每一个灯泡。26 位帧包含 6 位地址、8 位亮度值和 12 位颜色值。数据总线的菊花链拓扑允许模块化灯泡在灯串启动期间列举地址。有了这些信息，一个支持 5 伏电压的微控制器就能够以高达 24Hz 的刷新率控制一整串这样的灯。在这种情况下，[Robert]使用 ATtiny13A 微控制器来控制灯串。休息之后你可以看到他们的视频。

还拆开并分析了灯附带的无线发射器和接收器，揭示了廉价的 ISM 波段接收器和发射器模块对。也许它们会对另一个项目有用。我们期待着看到人们全年使用这些被黑掉的灯。

[通过[使](http://blog.makezine.com/archive/2010/11/hacking_led_christmas_lights.html)

[https://www.youtube.com/embed/AySja69jvHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/AySja69jvHM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)