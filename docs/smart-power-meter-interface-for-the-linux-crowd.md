# 面向 Linux 人群的智能电表接口

> 原文：<https://hackaday.com/2010/09/18/smart-power-meter-interface-for-the-linux-crowd/>

![](img/75ea2464c855a7e60583661b1fdadea6.png "power-meter-perl-interface")

[Graham Auld]从他的公用事业公司免费得到了一个能源监控器。插页中看到的设备提供了一个漂亮的 LCD 显示器，但他想要一种方法来绘制数据随时间的变化。有一根附带的电缆和一种使用 Google PowerMeter 的方法，但只适用于 Windows 电脑。他做了一点调查，想出了一个 Perl 脚本来连接仪表和谷歌的工具。

硬件模块被称为 [Current Cost CC128](http://www.currentcost.com/product-cc128.html) ，开发者很好地发布了一个 XML 输出描述，Graham 在他的脚本中使用了这个描述。从那以后，只需要通过[谷歌能量计 API](http://hackaday.com/2010/03/04/google-unveils-api-to-powermeter/) 进行注册和认证。该脚本尚未完全完善，但它可以作为您自己实现的路线图。