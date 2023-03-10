# LiPo 充电电路教程

> 原文：<https://hackaday.com/2012/01/28/lipo-charging-circuit-tutorial/>

就电池技术而言，锂聚合物电池是最好的。它们功能强大，足以处理要求非常苛刻的应用，并且有多种尺寸可供任何可想象的应用使用。然而，LiPos 有一个问题——当充电不正确时，它们有爆炸的倾向。幸运的是，【Paul】发来了一篇很棒的教程,介绍如何制作一个可以通过 USB 工作的 LiPo 充电器。

在【保罗】的板卡[原设计](http://asselinpaul.posterous.com/getting-those-lipos-charged)中，他选择了一个马克西姆 [MAX1551](http://www.maxim-ic.com/datasheet/index.mvp/id/4002) 锂电池充电器。困惑于这种 IC 的费用和/或不可用性(尽管 Sparkfun [有几个](http://www.sparkfun.com/products/674))，他转向了类似的微芯片 [MCP7813](http://www.microchip.com/wwwproducts/Devices.aspx?dDocName=en024903) 。这种 IC 支持从 3.5 到 6 伏的电源充电，就像 USB 集线器一样。

[Paul]设计的电路板非常小，仅仅比 USB 插头大一点点。布局也相当简单。我们认为这可能是一个非常有用的家庭板制造应用。如果你有一个更简单的方法来给吸脂器充电，不需要特殊的芯片，把它发送到[提示线](http://hackaday.com/contact-hack-a-day/)。