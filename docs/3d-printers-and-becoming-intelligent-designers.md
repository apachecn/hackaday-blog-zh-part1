# 成为聪明的设计师并拯救 RepRap

> 原文：<https://hackaday.com/2012/03/16/3d-printers-and-becoming-intelligent-designers/>

![](img/ecf977192fc4683f22f7ad963c99472f.png "RepVersus")

> 虽然黑客一天的工作方式是提供来自互联网各地的黑客，但有时我们觉得有必要行使一点编辑自由。一千字对于头版来说有点尴尬，所以请随意[跳过休息](http://hackaday.com/?p=69302)直奔这篇文章的全文。

众所周知，我和我的《Hack a Day》的作者们都对个人 3D 打印机的概念印象深刻。这些年来，我们已经看到[许多](http://hackaday.com/2012/02/29/new-extruder-3d-prints-tasty-treats-using-chocolate/)、[许多](http://hackaday.com/2012/02/23/multicolor-reprap-prints-the-really-really-hard-way/)、[建造](http://hackaday.com/2011/09/15/solar-powered-reprap-prints-even-when-the-power-is-out/)，3D 打印机是[一个重要的工具](http://hackaday.com/2012/01/06/3d-printing-minecraft-worlds/)或[建造本身](http://hackaday.com/2011/11/18/the-cheapest-and-easiest-3d-printer-weve-seen-so-far/)。

就个人而言，我喜欢拥有 3D 打印机的想法。在过去的几个月里，我建造了一个[Prusa Mendel](http://reprap.org/wiki/Prusa_Mendel)—[Sanguinololu](http://reprap.org/wiki/Sanguinololu)electronics，【Josef Prusa】的 PCB 加热床，还有一个非常漂亮的 [Budaschnozzle 1.0](http://reprap.org/wiki/LulzBot/Budaschnozzle/1.0) ，来自 [LulzBot](http://www.lulzbot.com/) 的了不起的人。我甚至用它制作了一些非常酷的塑料碎片，包括哥德尔、埃舍尔、巴赫的*封面内的 [GEB 立方体](http://hackaday.com/wp-content/uploads/2012/03/geb.jpg)(这是一个以物理形式实现的非常棘手的对象，但对我打印的第三样东西来说是一个不错的尝试，包括校准立方体)。现在，我正在为一个摇臂-转向架悬挂系统进行[车轮设计](http://hackaday.com/wp-content/uploads/2012/03/wheel.jpg)，我希望在八月初下一个火星探测器着陆时完成。我的 Prusa 是一个奇妙的工具；这不是一个堆满了磨机、车床和木工工具的车库，但这是一个开始。我认为它是 21 世纪的商店工匠。*

最近，我越来越意识到 RepRap 和 3D 打印机社区在不久的将来将不得不处理的问题，以及导致我写这篇小咆哮的可能解决方案。

#### 无限组合中的无限变化

如果我现在开始研究购买或制造什么样的 3D 打印机，我将面临比一年前更多的选择。即使我把自己限制在 RepRap 旗下的打印机上，我也需要在 [Mendel](http://reprap.org/wiki/Mendel) 、 [MendelMax](http://reprap.org/wiki/MendelMax) 、 [Prusa](http://reprap.org/wiki/Prusa) 或 [Mendel90](http://hydraraptor.blogspot.com/2011/12/mendel90.html) 衍生产品、 [Huxley](http://reprap.org/wiki/RepRapPro_Huxley) 、基于 Printrbot 的 [Wallace](http://reprap.org/wiki/Wallace) 、[这种简洁的折叠式 RepRap](http://reprap.org/wiki/FoldaRap) ，甚至是一种能够[打印自己案例的打印机](http://reprap.org/wiki/Tantillus)。

在“官方”RepRaps 之外，还有 Makerbot [Thing-O-Matic](http://store.makerbot.com/3d-printers/thing-o-matic.html) 、 [Replicator](http://store.makerbot.com/replicator-404.html) ，以及被弃用的 [Cupcake CNC](http://wiki.makerbot.com/cupcake) ，还有 [Makergear Mosaic](http://www.makergear.com/products/mosaic-3d-printers) 、 [Ulitmaker](http://blog.ultimaker.com/) 、 [SUMPOD](http://sumpod.com/) 、 [Printrbot](http://printrbot.com) ，以及 [UP！3D 打印机](http://pp3dp.com/)等等。

请记住，该列表并不完整，仅包括熔融塑料打印机的硬件，不包括[激光固化 UV 树脂](http://hackaday.com/2011/11/14/build-your-own-stereolithographic-3d-printer/)或[激光烧结](http://hackaday.com/2010/06/25/selective-laser-sintering-rig-on-the-cheap/)打印机。还有十几个版本的[电子板](http://reprap.org/wiki/Comparison_of_Electronics)，少量的[固件](http://reprap.org/wiki/Firmware)，以及几种适用于每台机器的[主机软件](http://reprap.org/wiki/RepRap_CAM_Toolchains#RepRap_Drivers)。简而言之，3D 打印机社区已经支离破碎，几乎无法修复。

#### 我们应该做什么

RepRap 之父艾德里安·鲍耶在近 10 年前提出了一个受生物启发的自我复制机器的想法。按照最初的设想，这个 RepRap 是一个[冯·诺依曼通用构造器](http://en.wikipedia.org/wiki/Von_Neumann_universal_constructor)的物理表现。[鲍耶]关于 3D 打印机作为通用构造器基础的想法模拟了生物生命和进化；一台为自己制造零件的机器随着一代比一代更有能力而“进化”。这个想法流行起来，大量丰富多样的 RepRaps 和其他 3D 打印机就像是寒武纪大爆发[中动植物的多样化。](http://en.wikipedia.org/wiki/Cambrian_explosion)

这种多样化并非没有进化的死胡同；像[自动化构建平台](http://www.makerbot.com/blog/2010/09/13/makerbot-automated-build-platform/)这样有用的附加组件被划分开来，只适用于 Cupcake 和 Thing-O-Matic。[用于无电脑打印的小键盘](http://reprap.org/wiki/LCD_And_Keypad_for_Generation_3)在电子板和固件版本之间并不总是可互换的。显然，需要有一个标准化；就像彗星撞入尤卡坦半岛一样，也许是时候将恐龙图案从地图上抹去了。

#### 无论如何会发生什么

在[阿德里安·鲍耶]对自我复制机器的设想中，[我们充当了类似病毒的复制体的宿主](http://reprap.org/wiki/BackgroundPage)，这些复制体自我复制并由人类组装。我们是引导新一代自我复制机器的进化力量。*是时候让我们像聪明的设计师一样行动了。*

我的建议很简单。让 [RepRap 核心团队](http://reprap.org/wiki/Admin)定义官方认可的 RepRap 标准。抛出一些设计供审查，比如 [Prusa 迭代 2](http://blog.reprap.org/2011/11/prusa-iteration-2.html) 、 [Makerbot 复制器](http://store.makerbot.com/replicator-404.html)和 [Printrbot](http://printrbot.com/) ，并从批次中挑选出最好的半打机器，并在它们上面贴上 RepRap 的名字。每六个月左右重复一次，逐步改进每个模型。让 RepRap 社区对每台机器充满信心。使“RepRap”成为通用商标。给 RepRap 这个名字赋予价值，这样在 50 年后，每个人的办公桌上都有“RepRap”了，而不是“一个熔融纤维制造快速成型设备”

#### 名字里有什么

有了半打 3D 打印机的设计，我们得到了什么？首先是来自世界各地的数百名爱好者、修补者和制造者的综合开发技能。数百人从事数百个设计带来的是一个线性的开发过程，并不能从整体上使项目受益。这是一种零敲碎打的方法，在重新发明轮子上投入了太多时间。

数百人致力于少数几个设计，将线性开发变成了指数级开发过程。有限的一组可能的机器意味着每一代每种型号都有更多的改进。如果 3D 打印机呈指数增长，那么 T2 也应该呈指数增长。

我们不仅会得到更直接的开发，而且将一套打印零件的模型交给中国的注塑工厂也变得可行，而不用担心“下周的模型”有了一套标准，RepRap 套件制造商可以投资工具来大规模生产套件，而不是依赖于装满打印机的货架来制造下一代套件。

#### 平行于视差

我的建议和另一个著名的开源项目有着惊人的相似之处。在 2005 年，[这个](http://arduino.cc/en/Main/ArduinoBoardSerial)就是 Arduino。只要看看 Arduino 在短短的七年里取得了多大的进步:有了 USB 端口，更好的微处理器，巨大的示例代码库，以及 Arduino Serial 和 Arduino Uno 之间减少的部件数量。Arduino 的开发仍在继续，现在已经有[以太网 Arduino](http://arduino.cc/en/Main/ArduinoBoardEthernet)和[电机屏蔽](http://arduino.cc/en/Main/ArduinoMotorShieldR3)提供了标准的硬件和软件库，供其他人改进。

Arduino 没有什么是新的；在 Arduino 出现之前的*年*，基本印记已经将微控制器和外围组件包装在一个封装中。现在，Arduino 在每个收音机小屋都可以买到，而像 [Handy Board](http://handyboard.com/hb/) 这样有能力的硬件则被降级为教育定价和教室的壁橱。所有这一切部分是由于 Arduino 团队定义了一个标准的板和 IDE。没有这些，Arduino 就不会有今天。

RepRap 很容易成为下一个纸巾、施乐、热水瓶或阿司匹林。只需要一个仁慈的独裁者来决定什么对我们所有人都是最好的。与 Arduino 一样，外设的开发和改进将会继续。最好的打印机将上升到顶端，我们将最终成为智能设计师 RepRap 允许我们所有人。

* * *

好吧，咆哮结束。这只是我已经讨论了一段时间的一个想法。如果你有反驳，或者想加入你自己的想法，请在评论中留言。我们现在把你带回到你的常规建设岗位上。