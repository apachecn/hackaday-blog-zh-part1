# 焊接站黑客增加温度控制

> 原文：<https://hackaday.com/2010/05/19/solder-station-hack-adds-temperature-control/>

拿起你称之为烙铁的廉价火棒，把它变成一个真正的工具。[Giorgos Lazaridis]通过在烙铁顶端增加一个热敏电阻来监控物体的温度，将他的 30 瓦烙铁变成了一个温控焊接站。MAX6675 负责热电偶，并向 PIC 16F88 发送数字温度值，PIC 16 f 88 通过从电位计接收用户输入并在 HD44780 字符显示器上显示设置来控制该单元。他用 ATX 供电公司内部解剖过的“墙麦芽汁”作为电站的外壳，这是一个巧妙的手法。休息后看它融化了剪辑中的一些金属。

这是对我们的焊接站导轨的一个很好的升级，它有一个温度控制的熨斗，但是缺少这里看到的传感器和自动化。

[https://www.youtube.com/embed/dA97AWkvwWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/dA97AWkvwWI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)