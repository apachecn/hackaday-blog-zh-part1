# 构建一个带有 Web 界面的留言板

> 原文：<https://hackaday.com/2011/08/19/building-a-message-board-with-a-web-interface/>

![](img/da4ecad15169a8000b3bbb12517898ac.png "message-board-with-web-interface")

[塞尔吉奥]刚刚进入硬件黑客。他首先在 Arduino 上安装了一个兼容 HD44780 的液晶显示屏。为了让这个项目更上一层楼，他决定[增加一个网络界面来改变 LCD 上显示的信息](https://sites.google.com/site/sergiosprojects/web-enabled-lcd-messageboard)。

他做事很便宜(正合我们心意)，从易贝购买许多零部件。不幸的是，当他要将 Arduino 接入网络时，这个决定反过来咬了他一口。以太网屏蔽山寨版与官方版本不一样。它有一个 Wiznet W5100 以太网芯片，可以为您做很多繁重的工作。相反，[塞尔吉奥]使用的是一块带有 ENC28J60 的板子。这需要一点搜索，但最终他想出了一个例子来帮助他获得 Arduino 服务网页并监听来自它们的更新。

ENC28J60 实际上是一个不错的硬件。它足够便宜，而且有一些硬件/软件演示值得一看。