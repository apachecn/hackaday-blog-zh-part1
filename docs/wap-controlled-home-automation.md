# WAP 控制的家庭自动化

> 原文：<https://hackaday.com/2008/12/22/wap-controlled-home-automation/>

![homeauto](img/c9beb98a846e5632f46d5d27a4eeb3ed.png "homeauto")

[Josh]提交了他不久前做的一个家庭自动化项目。它总共有八个开关插座。该项目的主要焦点是从任何手机的 WAP 访问远程控制。控制箱是基于由[Ashley Roll]设计的用于[使用 PIC](http://www.digitalnemesis.com/info/projects/picservo/ "PICServo Controller")微控制器控制八个伺服系统。用 Java 编写的监听器应用程序监控控制网页，并通过串口向板卡发送信号。他为每个插座使用光隔离 240V 固态继电器。所有的部件都可以在网站上找到，如果有足够的兴趣，他甚至可以做一个定制的控制板设计。