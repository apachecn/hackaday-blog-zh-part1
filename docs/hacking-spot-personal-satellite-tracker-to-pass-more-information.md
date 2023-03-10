# 黑客 SPOT 个人卫星跟踪器传递更多信息

> 原文：<https://hackaday.com/2011/10/01/hacking-spot-personal-satellite-tracker-to-pass-more-information/>

![](img/d93d98cb8b49aeac822feb32f85a2a1f.png "hacking-the-spot-satellite-transmitter")

不到 100 美元，你就可以买到一个小的跟踪模块，它会把你的位置上传到卫星上。但是你只会得到经度和纬度的信息。[naturam 42]花了一些时间对硬件和通信协议进行逆向工程，以[允许使用 SPOT 模块](http://natrium42.com/projects/spot/)传输自定义数据。

硬件的固定费用包括一年的服务计划，允许你在 SPOT 网站上使用你的设备[。[钠 42]开始在传输的数据包中打探，并认为如果他有办法将其编码为有效的纬度/经度包，他可以推送自定义信息，如海拔数据。他发现位置数据是以两组三字节的形式传输的。每组的四个最低有效位被服务器舍入，在两个数据集之间留下总共 40 个可用位。他编写了编码和解码功能，可以让你传递任何你想要的信息。](http://www.findmespot.com/en/index.php)

那么这有什么好处呢？为了让这个过程正常工作，他从电路板上取下了 MSP430 微控制器，并使用了自己的替代品。因此，您可以从板载模块、自己的模块传输 GPS 数据，或者将任何能够连接到替代 uC 的传感器数据。