# 电子尿布包提醒你打包除了婴儿以外的所有东西

> 原文：<https://hackaday.com/2011/03/15/electronic-diaper-bag-reminds-you-to-pack-everything-but-the-baby/>

![lilypad_diaperbag](img/a2a77b2d8e4f37342b92ea0acf09e328.png "lilypad_diaperbag")

[jnorby]知道带着孩子离开家是什么感觉，只是意识到她把她需要的东西忘在家里了。她不再依赖纸质清单，而是决定制作自己的尿布包，如果她忘记打包某样东西，尿布包会提醒她。

她从零开始制作她的包，将小电路连接到她在包内制作的每个口袋中。电线连接到按扣的每一半，这样当按扣接触时，它们就完成了电路。然后将 LED 和 snap 连接到 LilyPad Arduino，它会检查 snap 电路的状态，一旦合适的物品被打包，就会点亮相应的 LED。

虽然我们喜欢使用功能指示器提醒你打包物品的包的想法，但我们确实认为使用 Arduino 或任何微处理器都是大材小用。我们将放弃簧片开关的 LilyPad 和按扣，或者可能是常闭微型叶片开关，一旦包装好合适的物品，就会关闭 led，而不是相反。