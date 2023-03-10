# 自行车教练电脑:速度，节奏，心率，教练温度

> 原文：<https://hackaday.com/2010/01/12/bike-trainer-computer-speed-cadence-heartrate-trainer-temp/>

![](img/552f21ed6ec44d89fc06f825e9409dd2.png "bike-trainer-computer")

[Kurt]正在使用自行车训练器，以便在更暖和和更干燥的骑行月份中保持体形。不幸的是，如果你没有关于你有多努力的可靠数据，那就很难训练。教练电脑有商业解决方案，但他读了一些粗略的评论，然后[决定建造自己的教练电脑](http://etezadi.members.winisp.net/Bike/)。他在整合大量不同的数据收集来源方面做得很好。他拿起两个替换的自行车电脑传感器，用在后轮上测量速度(这种类型的教练前轮是固定的)，用在曲柄上测量节奏。他还戴着一个心率监测器，并采购了一个 [SparkFun 心率模块](http://www.sparkfun.com/commerce/product_info.php?products_id=8660)来收集数据。最后，LM235 模拟温度传感器与弹簧夹相结合，以检测教练阻力模块的温度。

来自传感器的数据由 PIC16F73 微处理器收集，并通过串行连接送入计算机。他有一个实时图表的截图，他在骑自行车时用它来获得反馈。这是一个有用且实用的设置，但是当他厌倦了锻炼时，他只需要几行代码就可以将其转换成游戏控制器。

[谢谢贾斯汀]