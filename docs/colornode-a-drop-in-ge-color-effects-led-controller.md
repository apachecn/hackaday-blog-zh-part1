# ColorNode:一个嵌入式 GE 颜色效果 LED 控制器

> 原文：<https://hackaday.com/2011/11/13/colornode-a-drop-in-ge-color-effects-led-controller/>

![colornode-ge-color-effects-controller](img/8f3e25091b2c880dabb441a9fd4bbf62.png "colornode-ge-color-effects-controller")

[Paul]今年想为他的节日装饰增添情趣，所以他买了一些 GE 色彩特效灯[并开始动手做。](http://www.digitalmisery.com/projects/colornode/)

我们已经看到这些 LED 灯泡对黑客是多么友好，这就是为什么[Paul]决定试一试。他的最终目标是从一个位置同步几组灯光，不幸的是，这需要他从他的控制板到每一根绳子走线。

然后，他决定走一条不同的路线，建立自己的控制板，作为通用电气控制器电路的替代产品。他想保留灯的无线控制方面，所以他选择了一些 RFM12B 无线模块，这些模块恰好得到了 JeeLabs 的支持。

他修改了他们的 JeeNode 板设计，使其适合色彩效果电子设备外壳，将它削减到控制灯光所需的最少组件。

ColorNode 的硬件已经完成，但是软件还在开发中。[Paul]说一旦他把事情搞定，他会把代码放到他的网站上。