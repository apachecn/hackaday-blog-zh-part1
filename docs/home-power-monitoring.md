# 家庭电源监控

> 原文：<https://hackaday.com/2009/07/05/home-power-monitoring/>

![powermonitor](img/dea3de85bc06de0c139bbe4972801adf.png "powermonitor")

读者[john]在假期周末完成了他的家庭电源监控器。它使用一对夹在电源上的电流传感器。这些输出为 0-3V，由 Arduino 的 ADC 读取。Arduino 对 20 秒内的样本进行平均，计算使用的功率，并使用以太网屏蔽上传。shield 不能进行 DNS 查找，所以他使用 WRT54G 与远程 web 服务器进行协商。他承认这个系统可以更精确；它不能检测像壁疣这样的小负载。他还说，通过与路由器进行串行通信而不是以太网通信，可以节省资金。这是[目前的使用图表](http://jarv.org/pwrmon_current.shtml "jarv.org")。

你可以在我们的 [Home Hacks 类别](http://hackaday.com/category/home-hacks/ "home hacks  - Hack a Day")中找到许多这样的电源监控器项目。