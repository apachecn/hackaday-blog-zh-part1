# CheapStat:一个开源恒电位仪

> 原文：<https://hackaday.com/2011/09/14/cheapstat-an-open-source-potentiostat/>

![](img/1cfca053ae4f81bc9873db9381bab7fa.png "CheapStatPhoto")

一个商用恒电位仪可能要花费几千美元，但是 [CheapStat 是一个开源项目，它可以让你以很小一部分的成本建造自己的](http://www.chem.ucsb.edu/~kwp/cheapstat/)。用不到 80 美元就能造出一台，打破了许多想要拥有这种测试硬件的实验室面临的成本障碍。

恒电位仪用于测量电化学性质。举几个它能做什么的例子，硬件可以测量水中的砷含量，橙汁中的维生素 C 浓度，非处方药中的对乙酰氨基酚浓度，以及一系列其他不太容易解释的与化合物和 DNA 有关的测试。

该设备利用 Atmel XMEGA 微控制器，并通过 USB 连接到计算机。一个 Java 程序从硬件中获取数据，在你选择的计算机平台上显示测试结果。如果你在寻找所有血淋淋的细节，你不会对他们的期刊论文感到失望。