# 用回收的电子设备跟踪商用飞机

> 原文：<https://hackaday.com/2011/09/22/tracking-commercial-aircraft-with-salvaged-electronics/>

![ads-b_air_traffic_tracking_station](img/c723eae752543b160113dfd646a92f57.png "ads-b_air_traffic_tracking_station")

去年早些时候，[爱德华]开始利用他放在家里的旧电子设备的组件开发一个[飞机跟踪系统](http://www.lll.lu/~edward/edward/adsb/Very%20Simple%20ADSB%20receiver.html)。你可能知道，也可能不知道，大多数现代飞机使用 ADS-B 协议在 1090MHz 频段上连续广播它们的当前位置。[Edward]发现他的旧卫星接收器模块能够毫不费力地接收信号，并非常乐意分享他是如何做到的。

整个项目花费了他不到 5 欧元，需要前面提到的卫星调谐器以及 ATMega48 微控制器来解码 ADS-B 消息。当接收器连接到一个很好的天线和前置放大器时，他可以监听 200 公里半径内的飞机，但即使只有一根简单的电线，他也可以定位 25 公里以外的飞机。

原始的 ADS-B 数据并不是非常有用，所以[Edward]组装了一个小应用程序，为他在地图上标出附近的飞机。我们认为用 Google Maps API 做同样的事情不会太难。

如果你对组装自己的飞机跟踪接收器感兴趣，一定要访问他的网站——他有大量有用的信息，可能会对你有很大的帮助。

[谢谢，大卫]