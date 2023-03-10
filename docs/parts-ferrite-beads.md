# 零件:铁氧体磁珠

> 原文：<https://hackaday.com/2009/07/06/parts-ferrite-beads/>

![ferrite-bead.ii](img/39542dbd4ee088b92338f587ab3a824b.png "ferrite-bead.ii")

[铁氧体磁珠](http://en.wikipedia.org/wiki/Ferrite_bead)(照片中的 L1)通过将高频电源噪声转化为少量热量来过滤高频电源噪声。电源噪声会给许多器件带来各种问题，尤其是在模拟音频和显示电路中。

铁氧体磁珠很简单，但选择一种可能会令人困惑，因为爱好者通常不使用它们。如果省略铁氧体磁珠，大多数设计仍然有效，但磁珠非常便宜，没有理由牺牲它们提供的额外可靠性。休息之后，我们描述了如何为我们的项目挑选铁氧体磁珠。

铁氧体磁珠的额定电流、阻抗和电阻；请看这个[鼠标列表](http://www.mouser.com/Search/ProductDetail.aspx?qs=sGAEpiMZZMvgExXaNlWje3%252bUuZptDS8sff%2f6%252b36uVLk%3d)的例子。除非数据手册或电路要求特定的磁珠特性，否则我们选择额定电流足够大的磁珠，忽略阻抗和电阻值。

如果磁珠用于电源，我们确定电路将使用的最大可能电流，并找到一个额定值为该值两倍的磁珠。上周，我们计算了总线盗版的最坏情况下的电流消耗为 525 毫安，所以我们看了额定至少为 1000 毫安的珠子。我们用的是[这个](http://www.mouser.com/Search/ProductDetail.aspx?R=BLM21PG331SN1Dvirtualkey64800000virtualkey81-BLM21P331SG)，额定 1500 毫安，10 美分一个。

有时，铁氧体磁珠用于为电路的一个特定部分过滤电源。我们用一个专用的珠子来过滤 [DIY 数码相框](http://hackaday.com/2009/01/08/how-to-digital-picture-frame-100-diy/)上的 LCD 偏置电压，并用名片上的[网络服务器上的 ENC28J60 以太网收发器。这些部件只消耗几毫安，所以我们使用了一个更小的](http://hackaday.com/2008/09/25/web-server-on-a-business-card-part-2/)[200 毫安铁氧体磁珠](https://www.mouser.com/Search/ProductDetail.aspx?R=BLM21BB600SN1Dvirtualkey64800000virtualkey81-BLM21BB600SN1D)(0.11 美元)。

喜欢这个帖子？查看您可能错过的[部分帖子](http://hackaday.com/category/parts/)。想申请一个职位吗？请在评论中留下你的建议。