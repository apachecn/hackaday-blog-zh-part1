# electro droid——您的 Android 电子参考应用

> 原文：<https://hackaday.com/2012/02/10/electrodroid-your-android-electronic-reference-app/>

![](img/7e723755b8f3d5b0fe8461af7f868851.png "title")

本周早些时候，黑客伙伴迈克·内森(Mike Nathan)评论了 Adafruit 的新 iPhone/iPad 应用程序 [Circuit Playground](http://hackaday.com/2012/02/07/circuit-playground-an-electronics-reference-app-from-adafruit/) 。[对【迈克】的评论](http://hackaday.com/2012/02/07/circuit-playground-an-electronics-reference-app-from-adafruit/#comments)转向建议 [ElectroDroid](https://market.android.com/details?id=it.android.demi.elettronica.pro&feature=search_result#?t=W251bGwsMSwxLDEsIml0LmFuZHJvaWQuZGVtaS5lbGV0dHJvbmljYS5wcm8iXQ..) 作为 Circuit Playground 的替代。令人惊讶的是，Hack a Day 的作者们实际上注意到了这些评论，所以我决定参与进来，提供我对 ElectroDroid 的评论。为了完全公开，我必须补充一点，我花了 2.59 美元买了一份不带广告的 ElectroDroid，并且没有和开发者接触过。

在打开的屏幕上，我看到了三个标签，分别是“计算器”、“引脚排列”和“资源”，每个标签下都有数不清的选项。与 Circuit Playground 相比，在一篇简短的博客文章中，有太多的选项可供全面回顾。在浏览每个标签时，我会尽量突出重点。

#### 计算器

![](img/de8aa05f4661827ab60be5f97feded2a.png "resistor1") ![](img/f455e0aa0fe2b63f443f724f8017094e.png "resistor2")

当然，ElectroDroid 允许您从颜色代码中计算电阻值，然后再反过来计算，并将从 SMD 电阻代码中获得电阻值。有趣的是，我找不到从电阻值到 SMD 电阻代码的计算器。虽然应用程序中有一个表允许值到 SMD 代码的转换，但我希望看到它能以更具交互性的方式实现。

![](img/64f991ca4e3d7217a8443dc898dd3cd5.png "555") ![](img/c96899735f22b49448a60da401314c6a.png "pcb")

其他计算器包括感应器颜色代码、欧姆定律、滤波器、分压器，以及其他列在 [ElectroDroid 网站](http://demisoft.altervista.org/_siti_interni/electrodroid/)上的所有东西。至于串联/并联电阻计算器，ElectroDroid 与[Mike]在 Circuit Playground 上看到的有些不同。像所有电阻计算器一样，你可以输入所需的值，让 ElectroDroid 从 E6 到 E192 系列中挑选出两个电阻，当它们焊接在一起时将与所需的值相匹配。此外，您可以输入两个电阻的值，并获得结果的并联或串联值。

与 Circuit Playground 不同，它允许以串行或并行方式放置 9 个电阻，ElectroDroid 将用户限制为两个。我认为 ElectroDroid 更能代表现实(为什么，确切地说，除了物理 102 作业之外，你还会有 9 个并联的电阻？)，但是使用*选项*来计算两个以上电阻的值会更好。

#### 引脚排列

![](img/5f4f4d73fcb4063e427c70f6f33766b9.png "25wire") ![](img/b8e770e8c7dcffbc88baf103dc4fd25e.png "OBD")

ElectroDroid 上的第二个选项卡是一个日常常见连接器的引脚列表。所有的常客都在那里——USB、串行(DE9 和 DB25 都是不错的选择)、并行端口、以太网和我见过的所有视频连接器。还有一些不常见但非常重要的 25 对电话线和 OBD-II 汽车诊断系统图。

这是一个很难审查的类别。很容易抱怨没有超级任天堂控制器的引脚，也没有我的旧 MAC 上的 ADB 或 25 引脚 SCSI 端口。对我来说，因为没有包括极其深奥的连接器而扣分是错误的；ElectroDroid 在包含 99%的制造商或建筑商需要的引脚方面做得非常好。在这里，ElectroDroid 发挥了它的作用。

#### 资源

![](img/09f6f245b45fa1c36f3b7814aff60428.png "7400") ![](img/9059359797d827dcbd8afa7812921d1f.png "resources")

在“资源”标签下，迎接我的是一张 19 项我应该已经记住的东西的清单。PIC 和 AVR 编程器的连接位于第一个位置，随后是标准电阻、电容、原理图符号、开关图(SPST、DPDT 等)、布尔逻辑符号的表格，以及 78xx 稳压器引脚排列的非常好的参考图像。

资源标签包括一个到 ChipDB 的链接，一个我承认从未听说过的网站。对于任何正在寻找整个 40xx 和 74xx 逻辑系列引脚的人来说，这是一个受欢迎的功能，但在撰写本文时，ChipDB 的数据库中只有 311 个条目。我不能因为这个数据库的不完整而责怪 ElectroDroid 开发者(它甚至不是他的)，但我希望在这个链接下看到更多的条目。

#### 最后…

当评论一个应用程序或任何相关的参考资料时，需要区分它*是什么*和它*可能是什么。* ElectroDroid 是一款出色的工具和参考应用，99%每天向 Hack 发送项目的人都会非常欣赏它。如果我根据*可能成为*来评价 ElectroDroid，我会觉得有点空虚。

就像 Adafruit 的 Circuit Playground 一样，我很想看到拍摄电阻照片并让应用程序显示值的能力。一个电子参考工具的“杀手级应用”将是 alldatasheet.com 的前端，它包括搜索、保存和显示任何可以想象的元件的数据表的能力。

这些都是吹毛求疵、异想天开的想法，但丝毫不会影响我对这款应用的印象。ElectroDroid 不仅仅值 2.59 美元的价格；虽然它对于模拟专家或那些可以用线制作计算机的人来说可能不是非常有用，但对于偶尔需要参考工具的修补者或制造者来说，它已经足够了。

附录:因为从 Android 设备上获取屏幕截图是疯狂的，我也想为 [MyPhoneExplorer](http://www.fjsoft.at/en/) 添加一个推荐。它工作了。