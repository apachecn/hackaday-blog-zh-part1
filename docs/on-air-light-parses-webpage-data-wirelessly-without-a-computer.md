# On Air Light 无需电脑即可无线解析网页数据

> 原文：<https://hackaday.com/2011/03/04/on-air-light-parses-webpage-data-wirelessly-without-a-computer/>

![](img/b5252ac2767af7733c0416eb770a816c.png "xbee-webpage-parsing")

[马特·理查森] [建造了这个直播灯](http://blog.makezine.com/archive/2011/03/networked-on-air-light-for-streaming-broadcasters.html)来指示一个制作流媒体节目当前是否正在进行。尽管底部有明显的电线(这是一根电源线)，但他的发明是通过无线方式从互联网上获取数据。他使用 Xbee 模块和 Arduino 来实现这个目标。

除了灯本身，还有一个我们从未见过的基站。硬件是一个 [Digi ConnectPort Zigbee 至互联网网关](http://www.digi.com/products/wireless-routers-gateways/gateways/)。这听起来有点拗口，但它只是一个充当 Xbee 节点的盒子，便于它自己的以太网端口和网络中其他 Xbee 设备之间的通信。所以，你不需要电脑，但你需要一个以太网连接基站。【马特】正在 ConnectPort call [Xbee 互联网网关](http://code.google.com/p/xig/) (xig)上运行开源软件包。休息后观看视频，了解该软件包的配置。这很简单，如果你以前从未使用过 Xbee 模块，这将让你知道它有多简单。

[https://www.youtube.com/embed/xr5Na49FTS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/xr5Na49FTS4?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)