# 电子纸信息面板

> 原文：<https://hackaday.com/2012/01/13/an-e-paper-information-panel/>

![](img/cb65d49cb6c3275f20f259ed99d87045.png "paper")

未来几年，我们肯定会在旧货市场和旧货店找到各种各样的物品，这可能会很有用。[Chris]制作了一个安装在门上的电子纸显示器，让自己了解最新的事件。

硬件来自几年前[克里斯和他的朋友【Deian】得到的](http://www.positron.org/projects/h2/hardware.shtml)电子纸开发包。开发工具包一直放在一个积满灰尘的抽屉里，直到[克里斯]决定用它做点什么。他的门看起来像一个合适的调色板，[Chris]决定制作一个信息面板，显示日期、他的日历、天气和一些 RSS 源。

当时已经有一台 Gumstix 单板计算机连接到电子纸显示器上，所以[Chris]在他的服务器上写了几个脚本，将信息上传到纸显示器上。服务器将显示渲染为 800×600 分辨率的 PNG 图像，将其转换为 [PGM](http://netpbm.sourceforge.net/doc/pgm.html) 并为 Gumstix 进行压缩。Gumstix 上运行一个脚本，每五分钟从服务器下载一次图像，并将其显示在显示器上。

凭借电子纸令人敬畏的可读性和低功耗，我们很惊讶以前没有见过这样的项目。看来我们得等到 Kindles 开始出现在跳蚤市场了。