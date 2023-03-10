# 自动关闭 APC UPS 设备

> 原文：<https://hackaday.com/2012/01/12/automating-the-shutdown-of-apc-ups-devices/>

![ups-shutdown-device](img/b6202afe1d82e77fd38ada3462f99335.png "ups-shutdown-device")

[Ishan Karve]在某个古怪的世界工作，那里的建筑管理要求在每天晚上结束时关闭所有服务器和不间断电源。虽然对大多数系统管理员来说不可思议，但他别无选择，只能遵从。这意味着他的员工需要在下班前关机，由于他们经常一天工作 15 个小时，等待 Windows server 关机似乎是一种永恒。

作为一名优秀的经理，[Ishan]决定制造一种设备来为他们处理服务器和 UPS 的干净关闭。Arduino 板充当设备的大脑，通过串行端口与 UPS 通信并向其发出关闭命令。Arduino 还连接到办公室网络，使其能够向服务器发送 ARP 请求，以确定服务器当天何时完全关闭。为了防止由于网络连接问题导致的意外关机，[Ishan]在组合中添加了一个 RTC 模块，以便 Arduino 至少在晚上 8 点之前不会发出关机命令。

不用等着 Windows 来做它的事情，[Ishan 的]员工一旦启动服务器关闭程序就可以离开，因为他们知道他们完全符合房东的疯狂要求。