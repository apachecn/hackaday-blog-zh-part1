# 从 IT 部门的垃圾堆中构建的网络监控面板

> 原文：<https://hackaday.com/2011/11/30/network-monitoring-panel-built-from-the-it-department-junk-heap/>

![network-monitoring-panel](img/2ac2ed722faf174485b337cc6b24e030.png "network-monitoring-panel")

在 IT 部门工作的一个好处是，通常会有大量杂七杂八、功能不全的设备可供使用。[Vittore]有一台旧的液晶显示器坏了的笔记本电脑放在周围([谷歌翻译](http://translate.google.com/translate?sl=it&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Fwww.zen.pn.it%2F2011%2F11%2Fnetwork-monitor%2F))，所以他想他还不如让它做点有用的事情。用一个备用的桌面液晶面板和一些软件调整，他为自己建造了一个光滑的网络监控面板，挂在他的办公室里。

他把笔记本电脑精简到最基本的部分，并把它和一个液晶显示屏一起安装在一个有机玻璃外壳中。他让 Nagios 在他的办公室里运行一台服务器，在一些插件的帮助下，他创建了一个简单的 web 界面，向他展示了整个网络的拓扑结构。面板本身运行的是 Debian 的实时版本，每次启动时，他都会加载他的 Nagios 网页。

虽然能够即时查看每个联网设备的状态非常棒，但他并没有就此止步。在网上浏览时，他发现了一个简单的基于 USB 的性能监视器的图表，该监视器使用 PIC 来驱动一对 VU 计。他将计量表连接到 Nagios 监控的路由器上，这样他就可以实时观察办公室的带宽使用情况。

如果你有兴趣看看它是如何建成的，一定要看看由[Vittore 的]同事[Matthew]整理的 Flickr 照片集。