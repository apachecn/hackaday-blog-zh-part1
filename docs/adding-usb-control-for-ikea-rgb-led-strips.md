# 为宜家 RGB LED 灯条添加 USB 控制

> 原文：<https://hackaday.com/2011/08/19/adding-usb-control-for-ikea-rgb-led-strips/>

![](img/77b6392afc6377e15d424d1fb2103ff6.png "ikea-dioder-hack")

这是一个经过改造的 PCB，它给宜家 Dioder 提供 USB 控制。这是一款价值 50 美元的产品，配有四条灯带，每条灯带包含九个 RGB LEDs。库存控制器有一个颜色选择轮和几个按钮。[Rikard Lind strm]想用它来匹配环境光和他的电脑显示器的颜色——是的，它是[的另一个流光溢彩克隆](http://hackaday.com/2011/08/01/adding-ambilight-clone-system-to-your-home-theater-just-got-a-big-price-cut/)。

因为他手头已经有一堆 AT90USB162 芯片，所以他选择了那条路线。这些芯片有原生 USB 支持(他使用的是 LUFA 封装，这是一个流行的选择)，但没有板载 ADC。这意味着不需要来自原始控制器的电位计，因为没有简单的方法来读取它的值。移除它为他的附加 PCB 腾出了足够的空间。他还减少了最初驱动该单元的 PIC 微控制器，焊接到空的焊盘上，以便连接自己的电路板。成品放回原来的外壳，唯一可见的变化是增加了一根 USB 电缆。现在，他可以用自己编写的程序拨出颜色。

如果你想知道，它看起来像是一个新版本的控制电路相比[原来的 Dioder 黑客我们涵盖](http://hackaday.com/2009/12/29/ikea-dioder-hack/)。