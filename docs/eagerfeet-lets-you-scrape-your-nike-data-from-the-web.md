# EagerFeet 让你从网上抓取你的 Nike+数据

> 原文：<https://hackaday.com/2011/04/19/eagerfeet-lets-you-scrape-your-nike-data-from-the-web/>

![](img/2a2e665585c83463c00ee8b3805065ce.png "eagerfeet-downloads-nike-plus-data")

穿着带有 Nike+系统的鞋子的跑步者可以将他们跑步的 GPS 数据上传到专有网站。如果您已经使用这个服务有一段时间了，您可能不愿意切换到另一个支持该硬件的服务，因为您不想丢失历史数据。面对这个问题，【Robert Kosara】开发了一些能够抓取 Nike+数据的[软件。他不仅写了代码，还建了一个网站来展示它的工作原理。](https://github.com/eagereyes/eagerfeet) [EagerFeet](http://eagerfeet.org/) 可让您复制并粘贴您的 Nike+ ID，以便在谷歌地图上绘制地图。

数据是从 Nike+上刮下来的，组装成 GPX 文件，是 GPS 数据的备份。从那里你可以用它做任何你想做的事情。由于代码可以在 Git 存储库中获得，所以您自己的项目很容易依赖于它，并且如果将来需要更改抓取系统，仍然可以获得更新。即使你不想在自己的项目中使用 GPX 文件，如果你感兴趣的话，也可以在一些第三方运动跟踪网站上导入它们。

当然，你可以试着直接从你的 iPod 上下载数据。