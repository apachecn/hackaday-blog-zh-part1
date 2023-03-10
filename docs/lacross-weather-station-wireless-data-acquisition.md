# 拉克罗斯气象站无线数据采集

> 原文：<https://hackaday.com/2011/09/06/lacross-weather-station-wireless-data-acquisition/>

![hacking_wireless_data_transfer_lacross_ws2305](img/1309e125606c44aeb6f2530d280a56b9.png "hacking_wireless_data_transfer_lacross_ws2305")

Hackaday reader [equinoxefr]在我们的 flickr pool [上发布了一些图片，展示了他对他的 La Crosse WS2305 气象站所做的一些修改](http://www.equinoxefr.org/post/2011/09/03/ajout-dune-liaison-sans-fils-xbee-802-15-4-sur-une-station-meteo-technology-ws2305/) ( [谷歌翻译](http://translate.google.com/translate?sl=fr&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwww.equinoxefr.org%2Fpost%2F2011%2F09%2F03%2Fajout-dune-liaison-sans-fils-xbee-802-15-4-sur-une-station-meteo-technology-ws2305%2F))。在过去建立了其他基于路由器的气象站后，[equinoxefr]在其中一个路由器停止工作后，正在寻找一种更好的方法来收集天气数据。

手里拿着一辆全新的拉克罗斯 WS2305，他的目标是将拉克罗斯的数据传输到他在 XBMC 的 HTPC。他把气象站拆开，用示波器四处探测，直到找到从设备中检索数据所需的 TTL Tx 和 Rx 引脚。他将数据针连接到 XBee 无线发射器上，然后藏在空间站的电池盒里。

另一个 XBee 单元通过 XBee Explorer 板连接到他的计算机，他很快就可以从气象站读取数据。

虽然他不是我们在这里看到的第一个拉克罗斯气象站的黑客，但我们喜欢它的简单和干净。如果你感兴趣，一定要看看[的 flickr 流](http://www.flickr.com/photos/equinoxefr/sets/72157627458115253/with/6108848170/)，看看黑客攻击过程的更多图片。