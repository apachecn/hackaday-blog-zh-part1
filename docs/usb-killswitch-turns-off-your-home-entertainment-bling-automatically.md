# USB Killswitch 可自动关闭您的家庭娱乐设备

> 原文：<https://hackaday.com/2011/10/12/usb-killswitch-turns-off-your-home-entertainment-bling-automatically/>

![](img/b044cdcde3f2cdaa280bb8e756854b58.png "usb-triggered-killswitch")

最后，电视机背面的 USB 端口可以用来做一些有用的事情。[Don]正在使用这个附加设备来自动切断他的流光溢彩克隆体的电源。最初，他厌倦了每次关掉电视都要拔掉电源适配器，所以他加了一个开关。但是懒惰战胜了他，他决定他需要一个自动的方法。在探查了可用的连接后，他确定串行接口(通常用于设备服务)没有任何用处，但 USB 端口有用。他测量了电源总线的电压，当电视打开时为 5V，当电视关闭时为 0.15V。他发明了你在上面看到的电路，它使用 USB 连接来触发继电器，当电视打开时给[他的流光溢彩克隆](http://hackaday.com/2011/09/28/ambilight-clone-built-from-arduino-and-shiftbrite-modules/)连接电源，当电视机关闭时断开电源。

我们的梦想一直是有 XBMC 功能的设备，可以 Velcro 到电视后面，并通过 USB 端口供电。不幸的是[小猎犬董事会](http://hackaday.com/2010/05/27/gsoc-takes-on-xbmc-on-the-beagleboard/)在运行 XBMC 时还没有达到稳定的水平。我们的下一个希望是[的 AppleTV 2](http://hackaday.com/2010/09/30/the-new-apple-tv/) ，它可以运行 XBMC，但需要一些黑客攻击才能让它在 USB 端口上工作，这引起了人们对它在 5V 时会消耗多少电流的担忧。