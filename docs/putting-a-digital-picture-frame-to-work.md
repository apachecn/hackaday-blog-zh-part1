# 将数码相框投入使用

> 原文：<https://hackaday.com/2009/03/03/putting-a-digital-picture-frame-to-work/>

![picture-frame](img/956f53d186e49a49b3ba494bfc1fe46e.png "picture-frame")

[Tobe]和其他几个人分享住处，所以他[开发了这个工具来帮助他们交流](http://www.infolexikon.de/blog/samsung-spf-83v-info-system/)。使用三星 SPF-83v wifi 功能的相框，他为购物清单和信息等内容创建了一个中心位置。他使用 PHP 进行数据库访问，并使用 [gd](http://www.libgd.org/Main_Page) 将其全部写入图像。每隔 15 分钟就会运行一个 cron 作业，将更新后的图像推送到相框中。