# 复活 USB 电路损坏的手机

> 原文：<https://hackaday.com/2012/03/27/resurrecting-a-cellphone-with-blown-usb-circuitry/>

![](img/fea249ab8bba66ec36b02625f70deec5.png "OLYMPUS DIGITAL CAMERA")

[Script]相当幸运。设计他的手机的一名工程师在电路中加入了过压保护。当然，如果没有可用的服务示意图，您可能不会知道这一点。但是稍微搜索了一下，他就让自己的诺基亚 N900 的 USB 接口复活了。

现在[Script]已经在试验便携式太阳能，比如几年前以 25C3 为特色的系统。不幸的是，他犯了一个错误，将 12V 输入了 USB 连接器的 5V 轨道。在这个不幸的错误之后，手机将不再通过 USB 连接，或者给电池充电。luickly N900 是黑客社区的最爱(你可以在 Hackaday 这里看到[所有与 N900 相关的项目),【Script】找到了](http://hackaday.com/2011/12/12/nokia-n900-control-pad-is-perfect-for-gaming-on-the-go/)[他们的 N900 示意图页面](http://wiki.maemo.org/N900_Hardware_Schematic)。深入第四页，他找到了标记为 2.0A 的零件 F5300。他移除了 PCB 和屏蔽，并用万用表测试了该零件，以确认其熔断。一个快速的电线桥让手机再次充电，但[Script]计划在找到零件后尽快安装新的保险丝。

谁说这些设备不适合用户维修？如果我们能得到更多的服务图表，也许我们的设备会持续更长时间。