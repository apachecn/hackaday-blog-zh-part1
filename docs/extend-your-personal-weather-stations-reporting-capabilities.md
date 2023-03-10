# 扩展您个人气象站的报告功能

> 原文：<https://hackaday.com/2011/10/21/extend-your-personal-weather-stations-reporting-capabilities/>

![](img/5d11734ed0671afc48fa4fabe60b27db.png "extending-weather-station-reporting")

这种 Nexus 无线气象站有一系列天气传感器，您可以将其安装在室外，并在 LCD 屏幕上进行监控。它还能够通过 USB 传输数据，但这一功能仅在 Windows 中得到支持，配套软件还有许多不足之处。这里有一种技术可以让你通过[将数据流式传输到你的 Linux 系统或者直接传输到互联网](http://www.8devices.com/wiki_carambola/doku.php/carambola_pachube_nexus)来释放数据的潜力。

事实证明，通过 Linux 获取数据变得非常容易，这要感谢[一个叫做 TE923](http://www.fukz.de/2009/03/08/te923-tool-v04/) ( [翻译为](http://translate.google.com/translate?sl=auto&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwww.fukz.de%2F2009%2F03%2F08%2Fte923-tool-v04%2F))的包。通过 USB 连接基本单元，软件将下拉一串冒号分隔的数据，这将很容易使用您最喜欢的脚本语言解析。但是如果你不想把它和电脑联系起来呢？

这个项目更进了一步，使用了一个杨桃板。这是一块 WiFi 板，上面有一个 USB 端口。它运行 OpenWRT，所以让 TE923 运行起来就像构建包一样简单。最好的部分是，任何运行 OpenWRT(或 DD-WRT 等)的无线路由器。)并有一个 USB 端口可以替代此板。随着模块连接到工作站，数据被推送到 Pachube 网站作为[一个定制的网络读数](https://pachube.com/feeds/37785)。

[Thanks Saulius]