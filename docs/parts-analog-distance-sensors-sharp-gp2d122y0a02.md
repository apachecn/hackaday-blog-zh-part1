# 零件:模拟距离传感器(夏普 GP2D12/2Y0A02)

> 原文：<https://hackaday.com/2009/02/24/parts-analog-distance-sensors-sharp-gp2d122y0a02/>

[https://www.youtube.com/embed/iGiRK0vmcUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/iGiRK0vmcUw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

夏普 GP2D12 和 2Y0A02 红外测距仪输出与物体距离传感器的距离成比例的电压。GPD12 可以感应 10-80 厘米距离的物体，而 2Y0A02 的感应范围是它的两倍。

我们之前已经看过了[夏普 GP2Y0D02 数字接近传感器](http://hackaday.com/2009/01/05/parts-digital-proximity-sensor-sharp-gp2y0d02)。它只发出物体存在的信号，而 GP2D12 和 2Y0A02 测量到它们的距离。如果你有一个 GP2YoD02，它仍然可以[点击模拟输出](http://www.ladyada.net/rant/2008/10/quick-tip-analog-signal-from-a-digital-distance-sensor/)。下面我们将向您展示如何使用这些传感器。

![cct](img/12ede69e6235dfd31e8653831a9ea02a.png "cct")

**夏普 [GP2D12](http://www.acroname.com/robotics/parts/R48-IR12.html) ，10-80cm 模拟 IR ranger(Digikey #[425-2046-ND](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail&name=425-2046-ND)****，$12.81)。[数据表](http://document.sharpsma.com/files/GP2D12J0000F_SS_20060207.pdf) (PDF)。**

 ****夏普 [2Y0A02](http://www.acroname.com/robotics/parts/R144-GP2Y0A02YK.html) ，20-150cm 模拟 IR ranger(Digikey #[425-2062-ND](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail&name=425-2062-ND)****，$14.38)。[数据表](http://document.sharpsma.com/files/gp2y0a02yk_e.pdf) (PDF)。** 

我们用 5v 电源给传感器供电，如上面的原理图所示。我们将输出端直接连接到万用表上测量电压。数据手册还建议在电源和接地引脚之间连接一个 10uF [旁路电容](http://en.wikipedia.org/wiki/Decoupling_capacitor)，但我们在本次演示中没有使用它。

![gp2d12](img/3b86ad9a041d2b225d9e3a0a831ca9be.png "gp2d12")

该图显示了 GP2D12 的输出电压与物体距离传感器的距离之间的关系(数据手册第 3 页，图 6)。您可以在数据手册第 5 页的图 2 中找到 2Y0A02 的距离/电压曲线。有一个公式来确定与输出电压的距离，或者你可以使用一个简单的[查找表](http://en.wikipedia.org/wiki/Lookup_table)。

对于非常近的物体，输出是不可靠的，看起来是 5 到 10 厘米之间的小驼峰。有可能通过使用几个具有[重叠范围](http://www.acroname.com/robotics/info/articles/sharp/sharp.html#e8)的传感器来解决这个问题，或者通过放置传感器使得[没有任何东西可以进入最小范围](http://www.acroname.com/robotics/info/articles/sharp/sharp.html#e30)。

有关各种夏普近程传感器的详细讨论，请查看 Arconame 网站上的[夏普红外测距仪信息页面](http://www.acroname.com/robotics/info/articles/irlinear/irlinear.html)。

喜欢这个帖子？查看您可能错过的[部分帖子](http://hackaday.com/category/parts/)。想申请一个职位吗？请在评论中留下你的建议。**