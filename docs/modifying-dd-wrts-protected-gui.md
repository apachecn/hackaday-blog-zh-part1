# 修改 DD-WRT 的受保护图形用户界面

> 原文：<https://hackaday.com/2011/09/21/modifying-dd-wrts-protected-gui/>

![hacking_the_ddwrt_gui](img/27d59d8b360d38e1a33d1a8437fcb766.png "hacking_the_ddwrt_gui")

[Craig]总是忙于解构和浏览各种固件映像。这一次，他承担了修改 DD-WRT 软件包的任务，这是 SOHO 路由器的一个流行的替代固件。

虽然固件是在 GPL 下发布的，但[Craig]指出，从源代码开始构建相当困难。相反，他说典型的做法是从固件映像中提取文件，修改它们，然后重建映像。这适用于大多数情况，但是 DD-WRT GUI 文件受到保护，以防止被修改。

由于他的字典里没有“你不允许这样做”这个短语，[Craig]开始尝试是否可以绕过保护措施，修改 GUI 代码。使用 IDA Pro 和 readelf 花费了相当多的时间，但他最终能够提取、调整，然后将各个页面重新插入固件映像。

这个过程相当耗时，所以他开发了一个叫做 webdecomp 的工具，可以自动提取和重建 DD-WRT 的网页文件。如果你有兴趣打造一个定制的 Hackaday 品牌的路由器界面，就像上面显示的那样，一定要访问他的网站并下载一份 webdecomp。