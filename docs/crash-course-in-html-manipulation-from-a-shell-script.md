# 从 Shell 脚本进行 HTML 操作的速成课程

> 原文：<https://hackaday.com/2010/12/25/crash-course-in-html-manipulation-from-a-shell-script/>

![](img/700342b56a5ca15cfac3005134b5aa9f.png "linux-html-manipulation-via-shell-script")

当涉及到由用户输入生成的页面时，自动处理来自互联网的数据可能会令人困惑。例如，假设您想从使用搜索框后加载的页面中抓取数据。[Andrew Peng]发布了一个快速而肮脏的示例来帮助您编写自己的脚本。他使用的例子是在他经常光顾的一个网站上查看股票。他的过程概述了找到所有搜索提交到的链接，建立用于发送搜索字符串的方法，并获取结果数据。他解析它，如果它找到了他想要的，就发送一封电子邮件。但这可以用于很多事情，以任何你能想象的方式让它提醒你应该不是问题。也许我们会用这个给[的老鼠](http://hackaday.com/2010/12/19/hackaday-unleashes-a-troll-sniffing-rat/)增加一些功能。