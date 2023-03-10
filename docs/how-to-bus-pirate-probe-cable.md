# 如何:总线盗版探测电缆

> 原文：<https://hackaday.com/2009/07/02/how-to-bus-pirate-probe-cable/>

![cover](img/c135399b76d4e4fbe061dca66d49e079.png "cover")

更新，2009 年 7 月 4 日星期六:所有预订都已停止。

一根探针电缆可以很容易地将总线盗版者连接到电路上，从而进行黑客攻击。好的测试夹可以在狭窄的印刷电路板上快速连接，而不会造成短路。我们为 [Bus Pirate v2](http://hackaday.com/2009/06/25/how-to-the-bus-pirate-v2-with-usb/) 做了两条电缆，继续阅读我们的设计概述和零件供应商列表。

2009 年 7 月 3 日星期五是预购巴士海盗的最后一天。只剩下两天的时间来得到你自己的巴士海盗 T1，完全组装好并运送到世界各地，只需 30 美元。

**概述**

![cables.450](img/0eb5bd5def02b6adb958f918c4ac1fc1.png "cables.450")

我们使用这些电缆将总线盗版的 I/O 引脚连接到微芯片或测试电路。电缆包括一个 2×5 连接器、一根电缆和某种可连接的探针，如鳄鱼夹或测试钩。

灰色电缆(顶部)是一种“垃圾箱”电缆，我们从废弃零件和旧计算机硬件中回收了它。“昂贵”的电缆(底部)使用高质量和特殊定制的零件。

**2x5pin 母接头**

![](img/7c83d7395e19b6e55dea8089cd2c05a1.png)

总线盗版的 I/O 接头是两排五个 0.1 英寸间距的引脚。我们使用 2×5 的排列，因为 2×5 引脚[的母排线连接器](http://en.wikipedia.org/wiki/Ribbon_cable#Cable_connectors)很常见，也很便宜。我们决定不采用单排 10 针，因为连接器是一种昂贵的专业产品。

引脚名称如上所示，并丝网印刷在 PCB 底部。参见[总线盗版页面](http://www.buspirate.com)了解各引脚功能的详细描述。

![connector-comapre.450](img/c8e8df1053ff2b1d36cab30de7b6ac88.png "connector-comapre.450")

垃圾箱电缆使用旧 PC ISA 卡的 2x5pin 母连接器。

这种昂贵的电缆使用黑色连接器，配有加强型电缆支架。Mouser 有[灰色连接器](http://mouser.com/Search/ProductDetail.aspx?qs=sGAEpiMZZMvT7Of4ktfHLp7HEgRb%252bXNqM189BZwCjls%3d)(0.69 美元)和[黑色连接器](http://mouser.com/Search/ProductDetail.aspx?qs=sGAEpiMZZMvT7Of4ktfHLryB5cuqtTOwUtyVZIBqjDM%3d)(1.15 美元)。

![connector-apart.450](img/1f416742701c7bd549efb876289e7d00.png "connector-apart.450")

带状电缆连接器具有内部引脚，当顶部压到底部时，这些引脚会刺穿电缆。

**带状电缆**

![cables-compare.450](img/a381cd63ce68e88ca706e852934162a7.png "cables-compare.450")

标准 2x5pin 母连接器连接到 [0.05 英寸](http://en.wikipedia.org/wiki/Ribbon_cable#Cable_sizes) 10 股带状电缆。导线厚度通常为 22、24 或 26 AWG。我们认为 12 英寸(30 厘米)是一个有用的长度，不会碍事。

灰色带状电缆很常见。我们从一个旧的计算机连接器上回收了一块，你可能会幸运地找到一个已经连接了 2×5 连接器的连接器。

彩色编码电缆便于识别每个连接。DigiKey 有 [5 个脚段](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail&name=MC10M-5-ND) ($3.03)，Mouser 有脚段( [$1.16](http://www.mouser.com/Search/ProductDetail.aspx?qs=sGAEpiMZZMsJiFh04Lj2rqXP8f7Pzi2%2fH6f0Eu5UWzk%3d) 、 [$1.19](http://www.mouser.com/Search/ProductDetail.aspx?qs=sGAEpiMZZMsJiFh04Lj2rrQIKM9xOMEOhuPHGzW6dSg%3d) )。

带状电缆便宜且容易获得，但它容易缠结和扭结。一个真正好的探针可以使用一个带状电缆头连接到更粗的测试引线上。

**测试夹**

测试夹是电缆最重要的部分。它们必须易于定位，并与电路保持接触。鳄鱼夹有效，但是有很多暴露的金属会造成短路。专业测试夹有一个抓取器，可缩入探针，减少金属暴露。

*鳄鱼夹*

![gator.450](img/a94a74a22350351fb00eacde1249ed94.png "gator.450")

垃圾盒电缆有鳄鱼夹探针，我们把它们从测试引线[上拉下来，就像这些](http://cgi.ebay.com/40-ALLIGATOR-CLIP-TEST-LEAD-INSULATED-COLOR-JUMPER-WIRE_W0QQitemZ350216518161QQcmdZViewItem) (40 根引线，12 美元)。你也可以使用宽松的[红色和黑色夹子](http://www.dealextreme.com/details.dx/sku.6359) (20 个，2.30 美元)。

记得在将电线焊接到鳄鱼夹之前，将橡胶外壳放在电缆上，以后就不会这样了。在照片中，你可以看到我们的一些封面被裁剪以适合剪辑的前面，因为我们忘记了。

*圆形测试钩*

![barrel-hooker-action.forget](img/03ce9a13a358270fd7e8a07fe3681d8b.png "barrel-hooker-action.forget")

这是经典的圆体测试钩。这些非常适合抓取 0.1”引脚接头、电线和通孔元件的引线。挂钩通常太大，无法与表面贴装元件配合使用，而且圆形的机身很难在狭小的空间内安装多个挂钩。

![rndhook-open.ii](img/9da83b33f21b293fb007bfb2b9a2d44e.png "rndhook-open.ii")

测试挂钩易于定位。挤压探针以伸出单个金属钩，抓住某物，然后释放。挂钩缩回到探头主体内，将其固定到位，防止短路。

![rndhook-apart](img/6537931c99ef6f658a052ed42b6c6dc9.png "rndhook-apart")

大多数钩子都是通过将顶部拉离身体而分开的。将测试引线穿过盖子上的孔，并将其焊接到金属片上。当接缝冷却后，将两半部分推到一起。

[DigiKey](http://search.digikey.com/scripts/DkSearch/dksus.dll?Detail&name=461-1015-ND)(17.26 美元)和 [Fry 的](http://www.frys.com/product/32861#detailed)(14.95 美元)有 10 个一套的多色挂钩。Deal Extreme 有非常便宜的 10 包[黄色](http://www.dealextreme.com/details.dx/sku.7218)(2.30 美元)和[黑色](http://www.dealextreme.com/details.dx/sku.8391)(2.33 美元)，但评论说质量符合价格，所以多买一些(通过[ [haku](http://hackaday.com/2009/06/29/parts-shiftbrite-rgb-led-module-a6281/#comment-79694) ])。

*扁平测试镊子*

*![hooker-action.450](img/7327f56f96f83767f66968fc12123826.png "hooker-action.450")
*

镊子探针非常适合夹在通孔、表面贴装和许多较小芯片的引脚上。它们通常有一个扁平的主体，因此比圆钩探头更适合狭窄的空间。

![hook-open.ii](img/2d9412da63bdecf21731eef73d50904c.png "hook-open.ii")

这种探针用小镊子代替钩子。意外短路很少发生，因为镊子缩回时暴露的金属很少。

![hook-apart](img/1df7e36755ba2939ab1145130e771c9b.png "hook-apart")

大多数镊子探针可以拉开，里面有一个金属焊片。将一根电缆线穿过盖子上的孔，将其焊接到金属片上，然后将两半压在一起。

不同品牌的镊子质量相差很大，我们使用的是不知名的探针，它们容易弯曲或者抓得不好。E-Z-Hook 的 [X 系列微钩](http://www.e-z-hook.com/Html/MicroHooks.html)是镊子探针中的佼佼者，我们首先使用了带有[salae 逻辑](http://hackaday.com/2009/03/06/tools-saleae-logic-logic-analyzer/)的 XKM 版本。它们旨在安装专业测试引线，但也很容易将电线焊接到其上。每个大约 2 美元，可直接从 [E-Z-Hook 网站](http://www.e-z-hook.com/Html/OrderingInformation.html)购买。

**结论**

我们强烈建议使用带钩或镊子探头的电缆，以确保连接安全，不会造成短路。正确的探头取决于您使用的零件。圆形测试钩最适合通孔零件和电线。扁平测试镊子可以很好地附着在小型表面贴装芯片上。

请在评论中分享任何额外的器件来源。我们尽了最大努力提供各种来源，但还是会有一些我们错过的好地方。

2009 年 7 月 3 日星期五是预购巴士海盗的最后一天。只剩下两天的时间来得到你自己的巴士海盗 T1，完全组装好并运送到世界各地，只需 30 美元。

![buspiratev2goii450](img/470775bf17d575b77a2322e5e630f5fb.png "buspiratev2goii450")