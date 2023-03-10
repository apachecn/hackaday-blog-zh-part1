# 只需几美元就可以制作一个二元挂钟

> 原文：<https://hackaday.com/2011/10/13/build-a-binary-wall-clock-for-just-a-few-bucks/>

![](img/f8773fe6292f405722ab4dd8266a6018.png "binary-wall-clock")

周末就要到了，如果你正在寻找一个下午的项目，考虑[建造你自己的二元挂钟](http://www.instructables.com/id/LED-Binary-Clock-1)。[Emihackr97]用手头的零件造出了你上面看到的这个，但是即使你把所有东西都下了订单，也不会花你多少钱。

他用一个纸板盒作为时钟的外壳，在表面标记一个 led 网格，并钻孔放置它们。两列表示小时，另外两列表示分钟，让时钟显示 24 小时时间，而备用固件显示 12 小时时间。由于有两个按钮——一个设置小时，另一个设置分钟——编写一点代码就可以通过同时单击两个按钮或按住一个按钮在两者之间进行选择。

[Emihackr97]使用 ATmega48 驱动显示器，atmega 48 是 ATmega168/328 的引脚兼容替代产品。这些芯片是 Arduino 板上最常见的类型，实际上这个项目正在运行 Arduino bootloader，但使用 ISP 编程器和试验电路板电路来保持低成本。有大量的引脚来直接驱动 13 个 led，使焊接快速而无痛。休息之后，请观看演示片段。

如果你在这方面做得很成功，并且渴望更有风格的东西，有很多方法可以让二进制时钟的外观更有味道。

[https://www.youtube.com/embed/XGLL9efyjjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XGLL9efyjjo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)