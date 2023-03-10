# circuit Playground——Adafruit 的电子参考应用

> 原文：<https://hackaday.com/2012/02/07/circuit-playground-an-electronics-reference-app-from-adafruit/>

![](img/8235db6a54fbf88a35c8ce6f77fa5164.png "circuitplayground")

我们并不是每天都在这里审查软件，但 Adafruit 的人最近整合了一个 iOS 应用程序，我想他们可能会感兴趣。他们的 iPad/iPhone 兼容应用程序被称为[“Circuit Playground”](http://www.adafruit.com/blog/2012/02/05/circuit-playground-adafruits-iphone-ipad-app-for-electronics-more/)，它包括各种方便的电子参考工具。在这篇评论的背景下，应该指出的是，我自己支付了应用程序的费用，并且我没有与 Adafruit 团队就我对该应用程序的评估进行过沟通。

正如你在主屏幕上看到的，该应用程序目前有八种不同的工具，不包括“Deals @ Adafruit”条目，因为我认为这更像是一种营销策略，而不是一种真正的工具。其余的项目是非常标准的参考票价，在一个易于使用和理解的包。

![mainmenu](img/dbdb031340559fa47f1aa9a59480fb08.png "mainmenu")

电阻值工具非常简单，允许您以两种方式指定电阻。您可以选择电阻器的色带并查看结果值，或者输入电阻值以查看您需要的电阻器颜色。如您所料，它支持 4 频段和 5 频段电阻，并具有一个简单的“说明页面”(与所有工具一样)，可通过屏幕左下角的小信息图标访问。我希望看到实现的一件事是拍摄组件并显示其电阻的能力。我认为对于视力不如以前的制造商来说，这将是一个非常有用的补充。

![resistortool](img/b552a7de269492b354a4547ef344765d.png "resistortool")

多电阻和多电容工具功能相似，显示各种串联和并联元件设置的合成电阻/电容。它们都支持多达 9 个项目，并允许您一次选择一个组件的电容和电阻值。这既有好处也有坏处，因为过一会儿手动输入每个值会变得相当繁琐。我认为可以改进的另一个项目是在串联和并联配置之间切换或添加/删除组件的功能。任何时候对配置进行更改，所有的值都会被重置–这意味着如果您在 8 电阻图中添加另一个电阻，您必须重新输入每个值。

![multiresistor](img/3355876d09cf1a76a7dcdd2ae7f64cb6.png "multiresistor") ![multicap](img/92d37218c51db513f0b15afcade0218d.png "multicap")

LED 电阻计算器就像它的名字一样，很像它之前的许多在线计算器。这个方便的功能允许您从预先确定的列表中选择 LED 颜色，根据一些常用/标准值自动填充正向电压和电流字段。指定电源电压和 led 数量后，应用程序会返回符合规格要求的确切电阻值，以及最接近的标准电阻值。虽然该工具在计算串联 led 的电阻时很有帮助，但它无法对并联配置进行同样的计算。如果 Adafruit 公司的人能够将这一功能与定制默认 LED 列表的能力结合在一起，我会非常高兴。然而，我必须指出，当改变 LED 颜色时，这个工具确实保留了 LED 计数和电源电压，这是我在玩了多电阻工具后很高兴看到的。

![ledresistor](img/b28a3bd9f78af24d3172a392112a2654.png "ledresistor")

欧姆定律计算器是一个简单的工具，它可以让我快速检查我在脑子里做过的数学运算。只需在三角形中输入两个值，Circuit Playground 就会输出第三个值。功率计算器是一个类似的简单工具，它接受四个值中的两个(功率、电压、电流、电阻)，为您计算其余的值。这两个工具都不太复杂，但是它们也不需要太复杂。

![ohmslaw](img/4a083a1df552c9f325fc0d818c2dc342.png "ohmslaw") ![powercalc](img/19c727d7dd0a71acd9ae6e53bab7577c.png "powercalc")

该应用程序提供的最终计算器使数字转换变得非常简单。给定一个数字，转换器将给出它的二进制、十进制、十六进制、八进制和 ASCII 表示法。虽然它可能不是我每天都会用到的东西，但它确实是一个非常有用的参考工具。我个人认为，这个工具将受益于转换字符串/数字的能力，而不是一次转换一个，但也许这是他们正在寻求在即将发布的版本中添加的东西。

![numberconversion](img/269476be6c292c1b986fa66ca7e6273a.png "numberconversion")

Circuit Playground 的一个不像主菜单上的其他功能那样突出的功能是内置的数据表查看器。它使用一个轻量级的界面来帮助搜索和查看 iPhone 文档存储中的 PDF 文件。我的手机上没有存储这种东西，所以我不能真正测试这部分应用程序——让我们在评论中知道它对你的作用。

![datasheetviewer](img/1f0da5e9ec4602aad277790394de54a2.png "datasheetviewer")

除了一些数据持久性的吹毛求疵，我认为 Circuit Playground 是一个很有潜力的可靠应用程序。售价 2.99 美元，位于 App Store 定价结构的高端，因此这些工具是否值得最终取决于你。Adafruit 确实表示，任何购买该应用的人都可以从他们在线商店的下一个订单中获得 3 美元的折扣，如果你是一名常客，这基本上使该应用免费。

虽然它不是为你的经验丰富的电气工程师设计的，但它绝对是兼职修理工的一个很好的资源。目前，这是一个仅支持 iOS 的产品，但 Adafruit 表示，他们将在未来的某个时候发布 Android 版本。同时，[他们建议试试 electro droid](https://market.android.com/details?id=it.android.demi.elettronica.pro&hl=en)，因为它是目前该平台上最好的应用。