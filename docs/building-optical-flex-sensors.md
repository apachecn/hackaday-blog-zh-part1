# 构建光学柔性传感器

> 原文：<https://hackaday.com/2011/10/21/building-optical-flex-sensors/>

![](img/3783dac814ab67272744a07980614411.png "optical-flex-sensors")

[Joel]翻出了他十年前做的这个黑客。它的灵感来自任天堂 PowerGlove，使用 flex 传感器对手指的运动做出反应。有趣的是，[他自己制造了这些光学弯曲传感器](http://coolshitindustries.com/2011/10/dataglove-with-ghetto-flex-sensors-circa-2000/)。

他喜欢说这是一个犹太人区光纤设置。上面的插图让你知道传感器是如何工作的。IR LED 和红外二极管位于一根透明水族管的两端。当灯管弯曲时，到达二极管的光量会减少，这种变化可以通过微控制器来测量。[Joel]发现他可以通过在试管中心添加一些东西来增加传感器的分辨率，在光线不直的时候阻挡光线。在这种情况下，他用的是废丝。传感器的外部也包裹在收缩管中，以防止环境光干扰测量。

他使用 trimpot 来调整传感器，但我们想知道在固件中添加校准算法会有多难？