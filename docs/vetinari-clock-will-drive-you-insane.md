# 维蒂纳里时钟会让你发疯

> 原文：<https://hackaday.com/2011/10/06/vetinari-clock-will-drive-you-insane/>

有时候我们生活中需要更多的心理战。作为 *Discworld* 系列的杰出粉丝，Reddit 用户【rdmiller3】决定他需要建造[维蒂纳里勋爵的时钟](http://www.reddit.com/r/arduino/comments/l1wwl/vetinaris_clock/)。在几本 *Discworld* 书中，这个虚构的钟被放在了维蒂纳里勋爵的等候室里。虽然这个时钟总体上保持准确的时间，但它有时会不规则地跳动，不同步。原因？削弱等待维蒂纳里大人的人的思想。

该建筑使用标准电池供电的模拟时钟。滴答机制只是一个安装在线圈驱动铁芯内的磁铁。线圈引线从时钟电路断开，并连接到 Arduino 的数字输入。通过几次 random()调用，时钟保持精确但随机的时间。

不幸的是，时钟在几个星期后停止工作，因为 Arduino 的 5 V 电压“太用力了”。[rdmiller3]说，尽管如此，几个电阻和发光二极管的压降会使电路更加可靠。休息之后，请观看难以观看的时钟运行视频。

[https://www.youtube.com/embed/KHKOhO_-hZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/KHKOhO_-hZY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

via [buildlounge](http://www.buildlounge.com/2011/10/05/the-vetinari-clock/)