# 极简的 RGB LED 立方体有一个非常短的 BoM

> 原文：<https://hackaday.com/2012/01/07/minimalist-rgb-led-cube-has-a-very-short-bom/>

![charlieplexed-led-cube](img/f0a63609b9c79000b137b56c232cfeab.png "charlieplexed-led-cube")

[Asher Glick]来信分享了他和他的朋友[Kevin Baker]一直在做的一个项目，一个 4x4x4 的 RGB LED 立方体。这两人是伦斯勒理工学院的学生，也是该校新成立的嵌入式硬件俱乐部的成员。作为他们的第一个合作项目，他们决定采用无处不在的 LED 立方体，将组件数量削减到不超过 64 个 LED、一个原型板、一些电线和一个 Arduino。

我们看到的许多立方体使用移位寄存器或十进制计数器来计算驱动这么多 led 所需的所有 I/O。他们版本的立方体没有这些额外的组件，而是完全依靠 Arduino 的 16 个 I/O 引脚进行控制。你可能还会注意到他们的立方体结构有些不同。他们没有像我们在大多数 Charlieplexed 立方体中看到的那样使用 LED 网格，而是使用 16 个 LED“尖塔”来构建他们的立方体，将额外的布线隐藏在电路板下面。

结果看起来很棒，你可以在下面的视频中看到。这个立方体看起来很容易建造，成本大约 60 美元，也是一个相当便宜的项目。

干得好，我们期待在未来看到来自嵌入式硬件俱乐部的各种有趣的项目！

[https://www.youtube.com/embed/yg0xVQmX5Co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/yg0xVQmX5Co?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) [https://www.youtube.com/embed/u9MJb3q-TBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/u9MJb3q-TBM?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)