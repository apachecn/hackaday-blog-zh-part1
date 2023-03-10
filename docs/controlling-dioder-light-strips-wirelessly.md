# 无线控制二极管灯条

> 原文：<https://hackaday.com/2011/08/25/controlling-dioder-light-strips-wirelessly/>

![dioder_universal_io](img/b0b12617f9fe39b8eafd323a15788b54.png "dioder_universal_io")

[SeBsZ]在家庭自动化方面做了大量工作，使用 Xbee 模块、led 和其他家庭照明系统。很自然，人们会在不同的电子项目上向他寻求帮助，但有一件事他已经被反复问过，那就是他是否能做出一个简单的[情绪照明解决方案，可以轻松安装。](http://www.sebsz.com/index.php?entry=entry110824-082449)

他一直对玩 RGB LEDs 感兴趣，但他并不打算在这个项目中重新发明轮子。相反，他的工作基于 Ikea Dioder 产品，一套现成的可调节 LED 灯条。[正如我们在](http://hackaday.com/2011/08/19/adding-usb-control-for-ikea-rgb-led-strips/)之前看到的，这些 led 的控制模块[还有一点需要改进](http://hackaday.com/2009/12/29/ikea-dioder-hack/)，所以他移除了 Dioder 的板载 PIC 并连接了自己的控制器。他的“通用 IO 板”使用 Atmega88 进行控制，并拥有连接 Xbee 无线模块所需的所有引脚。所有东西都装好后，他现在可以完全无线控制 Dioder 灯条，没有任何麻烦。

虽然他出售一些不同的硬件套件，但他的 IO 板的原理图可以在他的网站上免费获得，如果你想自己制作的话。我们唯一没看到的是 Atmega 的密码，但我们猜测他也把它贴在了某个地方。