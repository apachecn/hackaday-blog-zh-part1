# Arduino 子探测器

> 原文：<https://hackaday.com/2009/09/03/arduino-muon-detector/>

![100_0627](img/539915b14bce9689a00472b296f66fa6.png "100_0627")

塞巴斯蒂安·托姆扎克从他的朋友那里借了一台[homeadeμ介子探测器](http://hardhack.org.au/geiger_muller_detector)，并设法通过 Arduino 将其连接到他的电脑上。探测器本身使用 3 个荧光管来探测辐射。为了过滤掉地面辐射，使用了三个独立的管子；宇宙辐射将与管道成直线下落，并穿过至少两个管道，而地面辐射只会击中一个管道。有一些基本的电路来放大信号，然后执行“或”运算。

【Tomczak】用 Arduino 把原始数据输入他的电脑。然后他用 Max/MSP 分析数据，过滤掉背景噪音，只留下宇宙射线数据。不过，他没有提到他打算用这些数据做什么。也许他会把它连接到一个[合成器](http://hackaday.com/2008/11/17/auduino-software-synth/)。

相关:[数字盖革计数器](http://hackaday.com/2007/11/19/digital-geiger-counter/) 

[via @ [littlebirdceo](http://twitter.com/littlebirdceo/statuses/3731703331)