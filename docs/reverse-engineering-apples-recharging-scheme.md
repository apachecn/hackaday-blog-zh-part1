# 逆向工程苹果的充电方案

> 原文：<https://hackaday.com/2010/08/03/reverse-engineering-apples-recharging-scheme/>

[https://player.vimeo.com/video/13835359](https://player.vimeo.com/video/13835359)

【Ladyada】一直在努力工作[逆向工程苹果](http://www.ladyada.net/make/mintyboost/icharge.html)产品使用的充电方法。这个故事带我们穿越了这些年来新设备的发布和随后打破 [Minty Boost 的](http://hackaday.com/2006/05/31/minty-boost-aa-based-usb-charger/)充电功能。似乎数据线逐渐被 iPhones 和 iPods 用来识别连接的充电器。通过在 D+和 D-线上添加分压器，您可以指示手持设备为壁式充电器拉 1 安培(数据电压为 2.8v 和 2.0v)或为便携式充电器拉 0.5 安培(两条数据线均为 2.0v)。在上面的视频中，[Ladyada]从商用充电器上取下表面贴装电阻，以测量分压器并发现其中的秘密。