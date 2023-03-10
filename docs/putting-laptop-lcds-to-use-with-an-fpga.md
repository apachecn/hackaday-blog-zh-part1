# 将笔记本电脑液晶屏与 FPGA 配合使用

> 原文：<https://hackaday.com/2011/09/09/putting-laptop-lcds-to-use-with-an-fpga/>

我们总是对我们能够从垃圾中挑选出的笔记本电脑显示器的数量印象深刻。大多数时候，电脑已经坏得无法修复了，所以我们最终会有很多功能正常但无法使用的液晶面板。作为对我们所有人的服务，[爱因斯坦 _]发现了如何使用廉价的自制 FPGA 板来控制液晶面板。

LCD 面板不使用像 VGA 这样的简单协议来打开和关闭像素。取而代之的是使用非常高速的 [LVDS](http://en.wikipedia.org/wiki/Low-voltage_differential_signaling) 。LVDS 超出了简单微处理器的能力，所以[爱因斯坦 _]为自己建造了一个[XuLA FPGA 原型板](http://xess.com/prods/prod048.php)的克隆体，并开始工作。弄清楚面板的信号线后，[爱因斯坦 _]仔细研究了 LVDS 控制器和液晶面板的时序图。从数据表中，他发现数据通常以大约 500 MHz 的频率发送到面板。自制的 FPGA 板无法控制这样的速度，所以[爱因斯坦 _]将 FPGA 时钟减半。

虽然 LCD 的 60 fps 刷新率降低到了 30 fps，[EiNSTeiN_]说只有一点闪烁。对于一个很容易就被扔掉的东西来说，还不错。