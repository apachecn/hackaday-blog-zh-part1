# 简单的硬件和 Python 驱动这款 Splunk LED 仪表

> 原文：<https://hackaday.com/2012/03/02/simple-hardware-and-python-drive-this-splunk-led-meter/>

![](img/041bb3108cf786e5ae97da9f5bfc0c5c.png "splunk-led-meter")

想要在不持续加载 Splunk 仪表盘的情况下监控公司系统吗？原来他们有自己的 Python 包，使得下载数据变得轻而易举。所有[瑞克]需要做的就是[连接一个 LED 仪表作为外部显示器](http://www.richardosgood.com/2012/03/01/splunk-led-meter-complete/)。

过去，这需要很多电线和一些焊接(或者一些特殊的圣诞灯),但是价格实惠的 LED 灯的出现真的让猜测成为可能。他用的是从 Adafruit 公司获得的 RGB 版本。这些条带使用 SPI 驱动，多种颜色意味着您可以使用一列显示多维数据。他选择使用 Teensy 微控制器，抓取一些焊条的塑料包装作为外壳。这些条带非常明亮，为了帮助减弱冲击力，他在外壳内部添加了蜡纸作为扩散器。

寻找更多使用像这样的条带的项目？它们为你的家打造出奇妙的[可寻址重点照明](http://hackaday.com/2011/12/26/stripinvaders-puts-colored-lights-everywhere/)。