# 极简 LED 探光蜡烛

> 原文：<https://hackaday.com/2008/11/05/minimalist-led-light-detecting-candle/>

[https://www.youtube.com/embed/sPe5RtUOOdc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/sPe5RtUOOdc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

我们的[闪烁的 LED 电路](http://hackaday.com/2008/10/30/flickering-led-circuit/)结合了两个已知的电路，当然并不因此而优雅。[sprite_tm]看到了相当多的地区[可以减少电路](http://spritesmods.com/?art=minimalism)。他最终把它简化成只有两个发光二极管、一块电池和一个配件。第一步是去掉限流电阻。数据手册显示，采用 3V 电源时，AVR 会将电流限制在最大电流以下。接下来，光传感器被移除。[sprite_tm]参考了之前一篇关于用 led 感应[的帖子。他测量其中一个发光二极管关闭时的电压，以查看有多少光照射到它。开启时的电流消耗为 10mA，关闭时为 50uA。](http://hackaday.com/2006/02/21/low-cost-sensing-and-communication-with-an-led/)