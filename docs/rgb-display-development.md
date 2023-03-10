# RGB 显示器开发

> 原文：<https://hackaday.com/2010/01/17/rgb-display-development/>

![](img/404d62914114e1e9a28083de591ab1a2.png "large-scale-display-migrates-to-LED")

[SeBsZ]告诉我们[他正在使用 RGB led](http://www.sebsz.com/index.php?m=01&y=10&entry=entry100116-141613)制作显示器。他蚀刻了一些漂亮的表面贴装控制器板，以承载 ATmega8 微控制器和恩智浦 PCA9635 驱动器。这种设置使用 I2C 总线来寻址每个由 5 个 LED 模块组成的扩展板。理论上，这种硬件可以支持 638 个 RGB 模块，但由于功率和刷新率的问题，他的目标是达到 100-125 个之间，总共约 25 个扩展板。

还没到可以炫耀的地步。但是我们期望从这个项目中获得巨大的成功。部分原因是他的目标之一是生产一种可以卷起并容易移动的显示器，部分原因是他的大尺寸灯泡显示器令人印象深刻。休息之后看看他的 60 灯泡单元的视频。

[https://www.youtube.com/embed/plrybXfJZkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/plrybXfJZkw?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)