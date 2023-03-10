# 烤箱回流控制，无需改造烤箱

> 原文：<https://hackaday.com/2011/11/24/toaster-oven-reflow-control-without-modifying-the-oven/>

![](img/5296453a6e4839c359fcaca7db4e67b3.png "toaster-oven-reflow")

[Eberhard]想要自己的回流焊炉，但又不想摆弄控制加热元件的内部部件。他将自己的微控制器编程经验运用到工作中，设计出了一个[附加模块，通过切换主电源来控制烤箱](http://pleasantsoftware.com/developer/3d/reflow/)。

上图显示了处于回流过程中的电路板。如果你不熟悉，锡膏通常有一个推荐的热曲线来适当地熔化浆料。[Eberhard]设法将其中三个温度曲线放入他的固件中。

组成控制器的 ATtiny45 通过电路板旁边的热敏电阻对烤箱温度进行采样。PID 算法用于计算何时通过继电器打开和关闭主电源。一个按钮和一个 LED 组成了控制器的用户界面，用于滚动浏览三个预编程的温度曲线。

看起来效果很好，休息后在视频中自己看吧。

[https://www.youtube.com/embed/FvRv777KpxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/FvRv777KpxY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)