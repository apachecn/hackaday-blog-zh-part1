# AVR Dragon 布线替代方案

> 原文：<https://hackaday.com/2009/09/26/avr-dragon-wiring-alternative/>

![dragon_jumper_board](img/207af359d872bf9b7a469213b6fe1f02.png "dragon_jumper_board")

我们爱我们的 [AVR 龙](http://www.atmel.com/dyn/Products/tools_card.asp?tool_id=3891)程序员。这是一个具有许多功能的小型板:在线串行编程、JTAG、调试线和高压串行编程。不幸的是，开箱后它还没有准备好行动。Dragon 带有一个未填充的原型制作区域，并且缺少一个用于 HVSP 的管脚头。对大多数人来说，这意味着焊接引脚头和 ZIF 插座，然后在各种编程头和插座头之间跳跃。厌倦了用跳线工作，[Jussi]设计了[一个小 PCB 来做连接](http://translate.google.com/translate?js=y&prev=_t&hl=en&ie=UTF-8&u=http%3A%2F%2Fjuiceplatz.net%2Fblogi%2F2009%2F09%2Fvuosisadan-innovaatio%2F&sl=fi&tl=en&history_state0=)(芬兰语原文链接[)。](http://juiceplatz.net/blogi/2009/09/vuosisadan-innovaatio/)

![dragon_proto_area](img/2951a53e3d55afee515ecf9a47721187.png "dragon_proto_area")

上面你可以看到龙，因为它的船舶，与引脚头和 ZIF 插座添加，并与跳线原型。很容易理解为什么会有对替代品的需求。我们有一个[龙骑士 500 原型板](http://www.ecrostech.com/AtmelAvr/DragonRider/)，我们和我们的龙一起使用，但是【Jussi】觉得那个板对他来说有点太多了。

![dragon_jumper_sockets](img/2ec5620b9f7082d5182b5c62588701ac.png "dragon_jumper_sockets")

他的设计使用插头插座来连接 AVR Dragon 原型区域的引脚插头。它还连接一个晶体，并有一个跳线选择 USB 电源。这种解决方案需要为每种不同尺寸的芯片(8 针、20 针、28 针等)配备不同的适配器板，并且不利于连接外部电路。但是如果你只是需要对大量的芯片进行编程，这将把设置时间减少到仅仅几秒钟。