# LED 头盔是自由形式电路的漫威

> 原文：<https://hackaday.com/2011/07/17/led-headgear-is-marvel-of-free-formed-circuitry/>

Hackaday 贡献者[Nick Schulze]为一个帽子主题的聚会展示了一套令人印象深刻的 LED 头饰。

[Nick]对使用 led 并不陌生。之前他建造了一个蓝色的 8x8x8 立方体，类似于另一个 [512 节点全色版本](http://hackaday.com/2011/03/20/third-times-a-charm-512-led-cube-kicks-it-up-a-notch-with-rgb-leds/)。他有一堆那个项目遗留下来的发光二极管，决定把它们用在~~好的~~地方。

建筑的第一部分是框架本身，由粗铁丝网制成。他刚开始把它绕在头上，得到了一个不舒服的头状环，他可以在上面焊接。从那里，漆包铜线缠绕通过系统，为所有的 led 提供逻辑电平。一切都是在没有任何电路板的情况下完成的。LED 驱动器本身的连接方法是，首先使用拉链将一个电阻固定到框架上，然后将 TLC5916 芯片焊接到该电阻上。即使是 ATmega8 也被焊接到我们认为是服务器接地的框架上。编程它与自由浮动的女性引脚标题，你会得到精彩的动画在视频中看到休息。

[https://www.youtube.com/embed/7jMiPNVYAgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7jMiPNVYAgM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)