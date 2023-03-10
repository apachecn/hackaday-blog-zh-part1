# SMS 控制灌溉

> 原文：<https://hackaday.com/2011/02/12/sms-controlled-irrigation/>

![](img/d7909367cc49d68d1a4d346f48a2e901.png "sms-controlled-irrigation")

[Mhkabir]建造了一个通过短信交流的灌溉系统[。这个概念很简单，向系统发送一条短信就会使它打开水泵。](http://www.instructables.com/id/SMS-controlled-Wireless-Irrigation-System)

很多时候，我们看到[通过互联网](http://hackaday.com/2011/01/24/keyless-entry-via-sms/)操纵短信，或者[使用 GSM 模块](http://hackaday.com/2009/11/28/gsm-enabled-security-door/)。但在这种情况下，廉价的手机被用作通信接口。振动马达已被移除，并且这些连接被监控以发出传入消息。电线被焊接到键盘触点上，这样 Arduino 就可以在浇水出现问题时发送短信。这不是一个严密的系统，因为任何传入的消息都会触发系统，传出的消息仅限于已保存的草稿。但是一点创造性的编程，我们确信更多的功能可以从这个硬件中挤出来。