# 器件:0.1uF 去耦电容

> 原文：<https://hackaday.com/2008/09/29/parts-01uf-decoupling-capacitors/>

![](img/4c0330f202e9332ad455c25d151804d6.png "caps1")

大多数 [IC](http://en.wikipedia.org/wiki/Integrated_circuit) 需要从其电源[去耦](http://en.wikipedia.org/wiki/Decoupling_capacitor)，通常在每个电源引脚和地之间有一个 0.1uF 的电容。去耦通常用于消除噪声和平滑功率波动。每个项目都需要几个去耦电容；我们的[迷你网络服务器项目](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)有三个 IC，总共需要 11 个。这可能是单身人士购买的一个昂贵的部分，所以在网上储备是至关重要的。休息之后，阅读更多关于我们最喜欢的大容量通孔和表面贴装去耦电容的信息。

![](img/3425605531dc3dd8bdd43ed2311e64d2.png "caps2")

我们选择的电容应该足以满足大多数项目的需求。这三个部分的额定电压都是 50 伏，远远高于大多数数字电路。我们使用廉价的 20% [容差](http://en.wikipedia.org/wiki/Capacitor_(component)#Capacitor_construction)器件，因为去耦电容精确到 0.1uF 并不重要。更高或更低容差的电容也可以，但使用高质量去耦电容没有任何优势。这是上图中 0.1uF 电容的明细:

**C1** *通孔 0.1uF 电容*，如 Mouser #[594-k 104m 15 x7 RF 53 l 2](http://www.mouser.com/Search/ProductDetail.aspx?qs=9AX3phJxokWIpR5WRGtIJw%3d%3d)，(每 100 个 4 美元)——这种廉价的 0.1uF 电容将适合几乎任何需要通孔去耦电容的设计。引线间距为 2.5 毫米，并与默认 [Cadsoft Eagle](http://www.cadsoft.de) *rcl* 库中的 C-EU025-025×050 等封装尺寸相匹配。零件号-L2 有直腿， [-K2](http://www.mouser.com/Search/ProductDetail.aspx?qs=UCu6Cfgah1uC1E9iZgY2%2fQ%3d%3d) 有外部扭结，如图所示。

**C2** 我们建议你跳过 1206，直接去 0805。与通孔零件相比，1206 零件的成本优势微乎其微，因为它们不再是工业界的宠儿。0805 只是稍微小一点，但价格是它的一半。符合默认 *rcl* 库中的 Eagle footprint C-EUC1206。

**C3** 我们所有的新设计，表贴和通孔，都集成了这种非常便宜的去耦电容。符合默认 Eagle *rcl* 库中的封装 C-EUC0805。

查看我们之前在 [LM317 可调调节器](http://hackaday.com/2008/09/22/parts-lm317-adjustable-voltage-regulator/)和[触摸开关](http://hackaday.com/2008/09/15/tact-switches-for-your-next-project/)上的[部分](http://hackaday.com/category/parts/)帖子。你有什么需要我们帮忙的吗？