# 反向工程 USB 驱动程序

> 原文：<https://hackaday.com/2009/08/20/reverse-engineering-usb-drivers/>

![luxeed_keyboard](img/599fc4aabe105e045241f331d70a8000.png "luxeed_keyboard")

当[Jespersaur]购买了一个 [Luxeed LED 键盘](http://www.thinkgeek.com/computing/keyboards-mice/a85c/)时，他失望地发现驱动程序不是开源的，不支持他想要的所有功能。他的解决方案？[黑掉自带的驱动](http://www.jespersaur.com/drupal/book/export/html/21)，实现自己的。在他的文章中，他给出了用多种方法开始逆向工程的基本纲要，并简要介绍了 [libusb](http://www.libusb.org/) 。对于 Linux 驱动程序，查看[Kurt Stephens]的[站点](http://kurtstephens.com/luxeed)，在那里他提供了源代码的链接、构建它的说明以及向键盘发送命令的教程。