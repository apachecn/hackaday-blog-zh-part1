# 如何制作数字合成器

> 原文：<https://hackaday.com/2008/05/01/how-to-make-a-digital-synthesizer/>

![](img/d8534d9737d589c9aac391d82bde033f.png)

本周的指南来自我们的最新撰稿人:洛根·威廉姆斯。

这篇简单的指南将向您展示如何构建一个数字频率合成器来产生和处理方波。您的合成器将有一个振荡器，它产生由电位计控制的可变音高，以及一个以可变频率调制音高的 LFO。这个项目的零件数量很少，而且它的造价不到 20 美元。

## 寻找零件

制造这个数字合成器的第一步是[采购你需要的部件](http://www.hackaday.com/2007/11/16/how-to-where-to-find-parts-for-your-projects/)。这些大多可以在 [RadioShack](http://www.radioshack.com/category/index.jsp?categoryId=2032230) 买到，但 RadioShack 的价格往往比网上订购贵得多。这个项目的所有零件都可以在 [Jameco](http://www.jameco.com/) 、 [Digi-Key](http://digikey.com/) 或 [Mouser](http://mouser.com/) 购买。我们在下面提供了 Jameco 零件号。如果您不介意等待，这是订购零件的最佳方式。

![](img/f2402a45b6e758cbd6eec162971ea7d0.png)

| 项目 | 名字 | 无线电黑客 | 贾梅克 |
| 9V 电池夹 |  | [270-325](http://www.radioshack.com/product/index.jsp?productId=2062219) | $1.99 | [11280](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=11280) | $0.30 |
| 100K 线性电位计 | R2 | [271-092](http://www.radioshack.com/product/index.jsp?productId=2062287) | $2.99 | [255696](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=255696) | $1.35 |
| 1M 线性电位计 | R3 | [271-211](http://www.radioshack.com/product/index.jsp?productId=2062297) | $2.99 | [255582](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=255582) | $1.35 |
| 50K 线性电位计 | R4 | [271-1716](http://www.radioshack.com/product/index.jsp?productId=2062355) | $2.99 | [255549](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=255549) | $1.35 |
| 10K 线性电位计 | R5 | [271-1715](http://www.radioshack.com/product/index.jsp?productId=2062354) | $2.99 | [255522](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=255522) | $1.35 |
| 9V 电池 |  |  |  |  |
| IRF 510 MOSFET 晶体管 | 雌三醇环戊醚 | [276-2072](http://www.radioshack.com/product/index.jsp?productId=2062618) | $1.99 | [209234](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=209234) | $0.69 |
| 3.5 毫米音频接口 |  | [274-333](http://www.radioshack.com/product/index.jsp?productId=2062618) | $2.99 | [109496](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=109496) | $0.53 |
| 7805 5V 电压调节器 | IC1 | [276-1770](http://www.radioshack.com/product/index.jsp?productId=2062599) | $1.59 | [51262](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=51262) | $0.20 |
| 0.1 uF 电容 | C1 | [272-135](http://www.radioshack.com/product/index.jsp?productId=2062365) | $1.49 | [151118](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=151118) | $0.20 |
| 1.0 uF 电容 | C2 | [272-1055](http://www.radioshack.com/product/index.jsp?productId=2102515) | $1.59 | [544956](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=544956) | $0.20 |
| 40106 六角逆变器 | IC2 | [仙童](http://www.fairchildsemi.com/ShoppingExperience/action/displayItems?gpn=CD40106BC&itemType=SAMPLE) | $0.00 | [785071](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=785071) | $0.47 |
| 47K 电阻器 | R1 | [271-1342](http://www.radioshack.com/product/index.jsp?productId=2062349) | $0.99 | [690540](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=690540) | $1.00 |
| 1N4148 二极管 | D1 | [276-1620](http://www.radioshack.com/product/index.jsp?productId=2062587) | $2.59 | [1537969](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=1537969) | $0.27 |
| 无焊试验板 |  | 276-002 | $14.99 | [20723](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=20723) | $9.85 |

### 不是照片

| 项目 | 名字 | 无线电黑客 | 贾梅克 |
| 22AWG 实芯 |  | [278-1221](http://www.radioshack.com/product/index.jsp?productId=2049742) | $5.99 | [36792](http://www.jameco.com/webapp/wcs/stores/servlet/ProductDisplay?langId=-1&storeId=10001&catalogId=10001&productId=36792) | $6.59 |
| 扩音扬声器 |  |  |  |  |  |

### 工具

| 剥线钳 |

**注意**:电位计和音频插孔必须用胶带固定或焊接到 22 AWG 实芯线上。强烈推荐[焊接](http://www.hackaday.com/2007/10/26/how-to-introduction-to-soldering/)，因为它能产生更牢固的连接。

## 创建振荡器

在开始使用数字频率合成器之前，我们必须产生正确的电压。你们大多数人都熟悉使用 7805 5V 电压调节器。这很简单；将电池的+9V 连接到左手引脚，中间引脚接地，右手引脚为+5V。

任何合成器中最基本的电路是振荡器。方波振荡器不断在两种电压之间交替变化，在本例中为+5V 和 0V。我们有一个逻辑反相器来创建它，操作非常简单；如果它被给定+5V 输入(逻辑 1)，它给出
0V 输出
(逻辑 0)，如果它被给定逻辑 0，它给出逻辑 1 作为输出。当输入和输出连接在一起时，它会在这两个值之间快速振荡:0 进去，出来为 1，进去，出来为 0，以此类推。

问题是它振荡得太快了。可以添加一个电阻电容(RC)延迟电路来降低其速度。这迫使输出电流在到达输入端之前对电容充电。由此产生的短暂延迟将振荡减慢到可听频率。

要制造振荡器，在试验板上组装下面的原理图。

![](img/e10d997923848276f796c24ce648c201.png)

完成后，振荡器应该看起来像这样:

![](img/21efb7f6c10695c78f4ab0fcda8e3032.png)

把音频插孔的一边接到 0V，另一边接到输出，听起来会是这样的:

## 控制振荡器

我们可以通过允许用户改变频率来使事情变得更有趣。我们用电位计代替恒定电阻 R1，如 100K R2。这是一个简单的变化，并反映在这一改变的示意图。

![](img/c113092a336495070070293164a3501b.png)

![](img/70385079a679b535fe108b95ba2e091c.png)

现在振荡器听起来像这样:

有趣多了。如果你敢，试着演奏一首真正的歌曲。

## 占空比调整

我们可以添加一些基本的音色控制，使振荡器更有趣。方波的占空比是指它处于逻辑 1 和逻辑 0 的时间。例如，每个周期在+5V 时花费 1ms，在 0V 时花费 1 ms 的波将具有 50%的占空比。+5V 时为 1.5 毫秒，0V 时为 0.5 毫秒，占空比为 75%。为了调整波形的占空比，我们可以在电路中添加另一个电位计和二极管。当输入为高电平而输出为低电平时，电流将能够流过两个电位计，从而减少电容充电所需的时间，并提高占空比。

![](img/fb6a6e3d476b48409bf498635987aea5.png)

![](img/1b26904b7dad658d7a9891965c9c3fed.png)

完成后听起来应该是这样的:

## 创建 LFO

低频振荡器(LFO)是一种振荡速度非常慢的振荡器，每秒从 1 到 100 个周期。我们将使用 LFO 在两个不同的频率之间改变振荡器的音调。这可以用于声音效果、音色控制或音乐序列等警笛。

控制 LFO 的电路比我们以前用过的电路稍微复杂一些。因为它使用 10 倍电容的电容器和 10 倍电阻的电位计，所以振荡比我们的第一个振荡器慢 100 倍。LFO 连接到 IRF 510 MOSFET 晶体管的栅极。当 LFO 的输出为+5V 时，晶体管连接其源极和漏极引脚。连接这些引脚后，电流可以流过第二个电位计，从而增加螺距。当 LFO 回到 0V 时，电位计被断开，并且音高降回其原始水平。

![](img/8b2f18f66bcb4834fac2b8aed308ed66.png)

![](img/d8534d9737d589c9aac391d82bde033f.png)

LFO 可以发出很多声音，比如:

还有这个:

## 结论

现在，您已经制作了自己的简单数字合成器。不断尝试不同的控制方法。频率可以通过电阻来调节，因此几乎任何东西都可以用作输入。试试[光电池](http://www.engadget.com/2006/07/05/thingamagoop-the-synth-with-personality/)，或者[柔性传感器](http://createdigitalmusic.com/2005/08/08/hypersense-complex-gestural-gloves-for-music/)。尝试结合 LFO 和占空比调整。试着用它来制作音乐吧！我们很想看看你有什么想法。