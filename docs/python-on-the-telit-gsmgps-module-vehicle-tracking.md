# Telit GSM/GPS 模块上的 Python(车辆跟踪)

> 原文：<https://hackaday.com/2007/08/18/python-on-the-telit-gsmgps-module-vehicle-tracking/>

![](img/b1b1a368f17b050f3a641a5d742ef237.png)
【尼克】发现【亚历克斯】的[启用了 AVR](http://www.hackaday.com/2007/07/15/sms-tracking-with-a-gps-gsm-enabled-avr/)GPS，于是他使用相同的 Telit GM862 模块提交了他的项目。他不想依赖外部 AVR，而是想使用内置 python 解释器。显然，文档有点少，所以他整理了一篇关于为设备开发 python 的[好文章](http://www.digitaldawgpound.org/nick84/post=222)。由于 GPS 单元占用了以前用于调试信息的 com 端口，他添加了一个硬件 python 调试板来加速开发。

*   [永久链接](http://www.digitaldawgpound.org/nick84/post=222)