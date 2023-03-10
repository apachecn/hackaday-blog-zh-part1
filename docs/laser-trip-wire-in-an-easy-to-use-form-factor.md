# 易于使用的激光绊线

> 原文：<https://hackaday.com/2011/09/11/laser-trip-wire-in-an-easy-to-use-form-factor/>

![](img/cc09cc12766ae3f356036a8578182f74.png "laser-trip-wire")

[Rul]制造了一个漂亮的激光绊线报警器用于气枪比赛。只需将外壳放置在横梁穿过门口的位置，当横梁断裂时，它就会发出警报。这种设置的唯一问题是，在相反的一侧需要一个反射面，可以将光束引导回光敏电阻。但是等等，还有第二种选择。[Rul]还增加了一个叶片开关，可以连接到实际的绊线，而不是使用激光。

PIC 16F688 控制激光模块并监控光敏电阻和叶片开关。当第一次打开电源时，盒子进入设置模式，等待直到光敏电阻检测到激光，打开 LED 发出信号，表明光束瞄准正确。一按按钮，它就进入激活模式，当光束中断时，它会发出内部被黑的窗户警报。拨动开关让操作者在激光或焊线操作之间进行选择。

当闹钟响起时，你当然不会错过。休息后，看它在剪辑中把一只可怜的家猫吓得半死。

[https://www.youtube.com/embed/dB4jBeZ-wJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dB4jBeZ-wJs?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)