# 零件:LM317 可调电压调节器

> 原文：<https://hackaday.com/2008/09/22/parts-lm317-adjustable-voltage-regulator/>

每个项目都需要电源。随着 3.3 伏逻辑取代 5 伏系统，我们将触及 [LM317 可调稳压器](http://en.wikipedia.org/wiki/LM317)，而不是[经典 7805](http://en.wikipedia.org/wiki/78xx) 。我们已经为不同的情况找到了四个不同的爱好者友好的包。

一个简单的[分压器](http://en.wikipedia.org/wiki/Voltage_divider) (R1，R2)将 LM317 的输出设置在 1.25 伏和 37 伏之间；使用这个方便的 [LM317 计算器](http://www.cpemma.co.uk/317calc.html)找到电阻值。调节器尽最大努力将调节引脚(ADJ)上的电压保持在 1.25 伏，并将任何过高的电压转换为热量。不是所有的包装都是一样的。选择能够为您的项目提供足够电流的器件，但要确保封装有足够的散热性能来消除输入和输出电压之间的差异。

下面是上述电压调节器的细目分类:

IC1 [LM317LZ](http://www.mouser.com/Search/ProductDetail.aspx?qs=yAkVQ3mwCG1SXiMDnAr4Bg%3d%3d) 200mA，TO-92(0.59 美元)——这是最小的普通 LM317 稳压器。链接的部分可以提供 200mA，但 100mA 更常见。TO-92 封装会变得灼热，因为它不会散发太多热量。

IC2[lm 317t](http://www.mouser.com/Search/ProductDetail.aspx?qs=swDD%252bF%252bps7c8uLyY%252b3mJJw%3d%3d)1.5 安培，TO-220(0.64 美元)——在 1.5 安培时，这种调节器为大多数数字电路提供足够的电源。我们更喜欢表面贴装 D2Pack 版本(IC4)，因为我们不喜欢钻孔。TO-220 封装散发大量热量，如果您想要更多的冷却，金属标签将容纳一个散热器。如果您需要最大散热，请使用此封装。

IC3 [LM317MDCYR](http://www.mouser.com/Search/ProductDetail.aspx?qs=JS6RUWRH9DWKuMPAAfpOMw%3d%3d) 500mA，SOT-223(0.80 美元)——这是我们最喜欢的 LM317 封装。500mA 对许多项目来说都是足够的功率，小型 SOT-223 封装适合任何地方。

IC4[lm 317 d2t](http://www.mouser.com/Search/ProductDetail.aspx?qs=D1TrgBM0UaXEvjiszScJ1w%3d%3d)1.5 安培，D2Pack(0.83 美元)——当电路使用超过 400 毫安的电流时，我们使用 D2 pack 调节器进行设计。D2Pack 是 TO-220 的表面贴装版本，易于焊接。

所有 LM317 封装的封装尺寸都包含在默认的 [Cadsoft Eagle](http://www.cadsoft.de) *v-reg(电压调节器)*器件库中。

想了解更多关于 LM317 的信息吗？ [Instructables](http://www.instructables.com/id/The-Radioshack%2c-Adjustable%2c-Breadboard-Power-Suppl) 、【 [ladyada](http://www.ladyada.net/library/equipt/diypsupp.html) 、 [SparkFun Electronics](http://www.sparkfun.com/commerce/tutorial_info.php?tutorials_id=83) 有详细的 LM317 电源教程。