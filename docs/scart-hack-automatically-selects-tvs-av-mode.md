# SCART Hack 自动选择电视的 AV 模式

> 原文：<https://hackaday.com/2011/04/26/scart-hack-automatically-selects-tvs-av-mode/>

![](img/a8638845e73bfdabea23b247c9fa6d45.png "auto-av-select-for-xbox-scart-adapters")

我们确信仍然有很多人使用他们最初的 Xbox 来玩游戏或作为 XBMC 设备。如果你曾经拥有过一个，你会记得你不能用遥控器打开它。如果你必须站起来按下黑匣子前面的一个按钮，至少[这个软件会把电视调到正确的频道](http://www.instructables.com/id/Make-your-Xbox-switch-to-AV-mode-automatically)。也就是说，如果您使用 SCART 适配器将其连接到电视。

[Karl-Henrik]发现将一个电压映射到 SCART 端口的引脚 8 可以告诉电视该端口处于活动状态，并允许它选择合适的纵横比。查看维基百科 SCART 页面可以看到，推动 5-8V 是 16:9 纵横比的信号，9.5-12V 转换为 4:3。因此，他在 Xbox 的背面增加了一个音频插孔，并在适配器的塑料外壳上增加了一个匹配的插孔。现在只需接入内部硬盘电源连接器上的电线，将它们连接到新安装的插孔。有 12V 和 5V 线，根据你喜欢的长宽比选一个就行了。他用一根两端都有合适插头的跳线进行连接。现在，当 Xbox 启动时，电视会自动调谐到正确的 AV 输入。