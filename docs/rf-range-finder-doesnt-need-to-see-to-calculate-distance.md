# 射频测距仪不需要看来计算距离

> 原文：<https://hackaday.com/2011/03/21/rf-range-finder-doesnt-need-to-see-to-calculate-distance/>

![radio_rangefinder](img/0ab29b1fcb040dd918619f4c3b3e1564.png "radio_rangefinder")

Instructables 用户[琼斯电气]最近很忙，正在建造一个[射频测距仪](http://www.instructables.com/id/Distance-measurement-with-radio-waves)。作为德国青年科学竞赛的一部分，他和他的合作伙伴建造了一对发射器/接收器模块，可用于测量高达 1 英里(约 1.5 公里)的距离。他们支持无线电测距仪的理由是，激光测距仪显然受限于视线，而他们的测距仪则不然。

为了确定两个站之间的距离，基站被触发，它启动一个计数器并向第二个站发送 433 MHz 信号。当第二个站接收到信号时，它又广播一个 868 MHz 信号，该信号被基站接收。然后根据两个无线电信号的往返时间计算两点之间的总距离。

[琼斯电气]声称，测距仪相对准确，每次测量的偏差可达 5 米，并且可以通过在计时电路中添加更高频率的晶体来提高精度。

我们很确定在美国使用这两个频率是不被允许的，尽管我们不确定在德国的使用法律，这是哪里建造的。