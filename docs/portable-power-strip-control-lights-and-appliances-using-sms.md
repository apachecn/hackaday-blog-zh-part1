# 使用 SMS 的便携式电源板控制灯和电器

> 原文：<https://hackaday.com/2011/09/13/portable-power-strip-control-lights-and-appliances-using-sms/>

![sms_triggered_appliance_control](img/7798dff892f40c76fcb67bd6a7256d1f.png "sms_triggered_appliance_control")

[Julian]想要一种方法来远程控制他家周围的各种电器和灯，而不需要在家庭自动化上花费太多。他还希望能够轻松切换他正在控制的项目，而不会有太多麻烦。由于他找不到任何价格合理的东西来做他想要做的事情，他建立了自己的短信触发远程控制系统。

他将他的系统设计成像延长线一样使用，因此有了便携式接线盒外壳。这使他能够一次调节多达四个不同的项目，能够随意更换组件或重新定位他的控制器。

电源板由 Arduino 控制，Arduino 通过 Xbee 模块接收来自 PC 的命令。任何发送到他的 Gmail 账户的短信都会被他的电脑取回，然后传输到 Arduino。Arduino 反过来触发由[Julain 的]短信指定的继电器，利用 H 桥提供所需的电流。

如果你想在家里实现类似的东西，可以看看他的原理图和代码。