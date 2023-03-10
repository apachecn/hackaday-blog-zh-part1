# 建造 60 年代游击队自制方波发生器

> 原文：<https://hackaday.com/2011/12/03/building-a-60s-guerilla-homebrew-square-wave-generator/>

![](img/3684147ba5419053b9e2a29d34c1b89d.png "function")

当你有三个坏掉的函数发生器时，你会怎么做？[建立自己的](http://www.arthropodsystems.com/SquareWaveGenerator/SquareWaveGenerator.html)，很明显。由于你的工作室已经经历了三个这样的坏男孩，你可能会发现自己正在修复你的构建。最好不要使用任何花哨的集成电路，只使用[晶体管](http://www.arthropodsystems.com/SquareWaveGenerator/SquareWaveGenerator.html#mozTocId300432)制造。

当[Miroslav]送来他的“游击队自制”方波发生器时，我们真的印象深刻。相对简单的原理图使用了可以从旧收音机中回收的零件，这是一个真正的 MacGyver 版本。

该发生器基于一个简单的非稳态多谐振荡器。它不提供正弦波，但它是最容易工作的电路。构建从四个 2N4401 晶体管开始，但根据数据手册和古老的 Tektronix 502A，与 2N3904s 相比，这些晶体管的上升时间非常差。

[Miroslav]的项目产生高达 2.22 MHz 的方波和占空比在 1-49%和 51-99%之间变化的脉冲。输出为 5 伏 TTL 电平或可调的 0-3.38 电平。发电机正是[Miroslav]所需要的，所以在我们看来，它是一个很好的工具。