# WiFi 流媒体广播更新

> 原文：<https://hackaday.com/2009/02/03/wifi-streaming-radio-update/>

自从我们关于他的 [WiFi 流媒体广播项目](http://mightyohm.com/blog/2008/10/building-a-wifi-radio-part-1-introduction/)的[上一篇帖子](http://hackaday.com/2008/12/19/wifi-streaming-radio/)以来，【杰夫】一直在努力工作，以发布该项目的[第 8 部分](http://mightyohm.com/blog/2009/02/building-a-wifi-radio-part-8-adding-a-tuning-control/)，在那里他为广播添加了调谐控制。有趣的是，添加调谐控制只需要一个电位计和来自[第 7 部分](http://mightyohm.com/blog/2008/12/building-a-wifi-radio-part-7-building-an-lcd-display/)的完整 AVR LCD 板。将电位计连接到 AVR 上的模数转换器并添加几行代码后，收音机现在可以快速轻松地调谐了。除了全面解释硬件变化之外，[Jeff]还详细介绍了 OpenWRT 框架所需的配置变化，以便路由器和 AVR 之间的双向通信成为可能，从而允许调谐器正常工作。一定要看看上面的视频，看看调谐器的行动。