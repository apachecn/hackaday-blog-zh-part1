# 砰-砰你的方式到一个完美的蛋糕

> 原文：<https://hackaday.com/2012/01/05/bang-banging-your-way-to-a-perfect-cake/>

![bang-bang-oven-control](img/de5438f9782c75e99c7285e91811bcfa.png "bang-bang-oven-control")

罗布·斯潘顿的房子配备了一个相当便宜的烤箱，这是他的室友试图用它来烤婚礼蛋糕时发现的。如果有人在烘烤过程中洗澡，很大一部分单位的气体压力转移到锅炉，导致烤箱完全关闭。这显然不适合烤蛋糕，所以室友们决定建造一个临时控制器来保持温度一致。

他们首先在烤箱的旋钮上安装一个滑轮，滑轮通过一条长橡胶带连接到一个小马达上。皮带的另一端连接到一个小型电机，该电机由 Pololu 18v7 电机控制器控制。一个 K 型热电偶监测烤箱的温度，通过 MAX6675 转换器将数据输入(大概是)Rob 的电脑。

因为时间有点紧，所以[Rob]和他的室友[Johannes]决定让烤箱保持稳定温度的最好方法是通过 bang-bang 控制。虽然你可能会认为在最小和最大设置之间反复转动油门旋钮不是处理事情的理想方式，但他们的解决方案非常有效。蛋糕非常完美，整个烘焙过程中的最高温度只有 11.5 摄氏度——考虑到设置，这是非常合理的。