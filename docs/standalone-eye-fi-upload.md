# 独立视频上传

> 原文：<https://hackaday.com/2009/03/15/standalone-eye-fi-upload/>

![eye-fi](img/a903206086f8f7f802cf5e13ce37a40f.png "eye-fi")

前 Hack a Day 贡献者[Will]一直在使用一张[Eye-Fi](http://www.mahalo.com/Eye_Fi)sd 卡来让[自动传输他的照片](http://biobug.org/index.php/2009/03/14/hacking-the-eye-fi-to-keep-your-data-home/)。不幸的是，这需要使用 Eye-Fi 的软件并与他们的服务器通话。他用[Jeff Tchang]的用 Python 写的[替换服务器](http://returnbooleantrue.blogspot.com/2009/01/eye-fi-standalone-server.html)来接收卡片上的图像。[Will]使用[图库 2](http://gallery.menalto.com/) 管理自己的在线图片库。为了上传图片，他添加了一个对 GUP 的调用。现在，他所有的照片都可以像标准的目镜一样方便地传输，而不需要任何中间人。

[图片: [Eye-Fi 拆机](http://hackaday.com/2009/02/01/eye-fi-teardown/)