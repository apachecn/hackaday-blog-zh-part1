# 使用 IPhone 的电脑显示器睡眠模式

> 原文：<https://hackaday.com/2010/11/17/pc-monitor-sleep-mode-using-iphone/>

![](img/7770564eb617dd9e97db48b1932eace5.png "iPhone-makes-montior-sleep")

[迈克·西尔弗曼]想出了一个办法让他的显示器从 iPhone 上睡眠。他使用 Windows 系统，安装了 QuickPHP 和 NirCmd 来添加 PHP 和命令行控件。一些快速的 PHP 代码编写，这有创建一个通过网络地址切换的睡眠按钮的效果。他在 iPhone 的 Safari 浏览器中加载了 IP 和端口信息，创建了上图所示的主屏幕快捷方式。现在他点击按钮，让屏幕进入睡眠状态。

我们并不认为这个功能有用，因为大多数显示器在几分钟不活动后就会休眠。但是我们喜欢这种方法，你可以打赌我们已经在计划使用它了。任何 PHP 服务器(比如这台机器上运行的 Apache 的副本)都可以，只要它与 iPhone 的 WiFi 连接在同一个局域网上。