# 实时气体监控

> 原文：<https://hackaday.com/2008/09/21/real-time-gas-monitoring/>

![](img/8193bdddfa61440e6d5123815f614cc0.png "gas_meter")

随着天气越来越冷，[丹尼尔]决定实时监控他的燃气加热使用了多少能源是个好主意。他使用诺基亚 6680 照相手机通过观察窗监控加热器的火焰。 [PyS60](http://wiki.opensource.nokia.com/projects/PyS60) ，Python 的 Symbian 实现，检查摄像头发送的图像，测量有多少蓝色火焰可见。这些值存储在手机的 SQL DB 中，可以通过蓝牙进行轮询。在计费周期结束时，他将能够将使用的汽油量与手机报告的数据关联起来。

[谢谢你，佛罗伦萨巴耶]