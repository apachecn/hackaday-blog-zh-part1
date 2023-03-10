# 用水反馈改变行为

> 原文：<https://hackaday.com/2010/11/07/water-use-feedback-changes-behavior/>

![](img/7de4aa9d9fa759f810310ce06b96fd71.png "water-faucet-flow-sensor")

洗澡、洗手或洗碗时，你会用多少水？不是一般人用多少，而是你用多少？这就是蒂格实验室的团队开始用这个[用水反馈系统](http://labs.teague.com/?p=722)寻找的东西。使用的传感器是 Koolance 流量计，用于测量 PC 液体冷却系统中的冷却剂流量。售价 20 美元，它是一个很好的低成本传感器，配有 WiFi 功能的 Arduino。在上图中，他们用 iPad 作为屏幕，这样你就可以看到你洗手时用了(或浪费了)多少水。这使得人们每次洗手都能节约 1/2 加仑的水。

项目代码、原理图和电路板文件均可下载。除了硬件构建之外，还有一些很好的服务器端软件，可以随着时间的推移收集数据并绘制图表。我们已经看到了许多[电表黑客](http://hackaday.com/2010/09/21/another-approach-to-power-meter-data-harvesting/)，但是有跟踪用水的选项是很好的，即使这是为一次只有一个水龙头定制的。