# 从电池充电器获取更多信息

> 原文：<https://hackaday.com/2011/07/18/getting-more-information-from-your-battery-charger/>

![echo_6_battery_charger_serial_hacking](img/ea2ebe660c5c0cb081ec320c56e79bca.png "echo_6_battery_charger_serial_hacking")

[Dane]买了一个相当便宜的(17 美元)Hobbyking Echo-6 电池充电器，想看看他能从这个设备中获得什么样的信息。由于充电器是为各种电池化学物质设计的，并配有液晶显示屏，他认为它包含一个相当不错的微控制器，他可以从中获取一些有用的数据。

他拆开了装置，开始四处寻找有用的物品。他发现它使用了 ATMega32 微控制器，并且在 PCB 上有相当多的未填充区域，这使得[Dane]认为 Echo-6 与更强大的充电器共享其主板。他接入了 ATMega 的 UART，立即开始看到数据。一旦他发现串行线路上有什么，他就把数据输入 LogView，产生了一些漂亮的图表，详细展示了充电/放电过程。

对于任何技能水平来说，接入 Echo-6 似乎都很容易，我们认为任何人都可以从他们的电池充电器中获得某种信息。