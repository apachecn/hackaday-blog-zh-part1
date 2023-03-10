# LED 矩阵眼镜让所有的眼睛都盯着你

> 原文：<https://hackaday.com/2011/05/03/led-matrix-glasses-keep-all-eyes-on-you/>

![my_shades_are_so_bright_i_gotta_wear_um_something](img/ed1f3d199f63b9eea2f2bf2fa745d6ba.png "my_shades_are_so_bright_i_gotta_wear_um_something")

Instructables 用户[llopez-garcia]正在寻找一些能让他在音乐活动或俱乐部中脱颖而出的东西，并决定在一副太阳镜中内置一个 LED 矩阵就能达到这个目的。

他拿了一些发光二极管和一副他在沃尔玛能找到的最大的太阳镜，然后开始谈生意。他没有微控制器编程的经验，所以他选择了 PICAXE 20X2 来运行他的眼镜，认为用 BASIC 编程比用 c 编程更容易。

他在镜头上钻孔，连接两个 5×5 的 led 网格，将它们连接到 PICAXE 上，形成一个 10×5 的阵列。之所以选择这种设置，是因为 20X2 将他限制为 15 个可用引脚，并且他希望避免使用移位寄存器或 LED 驱动器来减少器件数量。其余的构建相对简单，在所有正确的位置安装电阻器，并使用一对 AAA 电池供电——每个太阳穴绑一个。

我们认为这很酷，尽管我们不确定他戴着它是否能看到任何东西。话说回来，谁在乎呢？你不需要戴着这么棒的眼镜也能看得见。

如果他必须从头再来一遍，[llopez-garcia]说他会稍微加强一下 LED 结构，并选择一个可以用 C 编程的不同的微控制器，因为他觉得 PICAXE 有点受 BASIC 的限制。

留下来看看这款眼镜的快速演示视频。

[https://www.youtube.com/embed/69aoLjXfhdQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/69aoLjXfhdQ?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)