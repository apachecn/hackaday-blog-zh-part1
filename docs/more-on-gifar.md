# 更多关于吉法尔的信息

> 原文：<https://hackaday.com/2008/08/06/more-on-gifar/>

![](img/0c2135e7f9b21b6367fa55b427ed8759.png)
【PDP】提供[一些](http://www.gnucitizen.org/blog/gifars-and-other-issues/) [关于](http://www.gnucitizen.org/blog/more-on-gifars-and-other-dangerous-attacks/)[新闻](http://www.hackaday.com/2008/08/04/the-gifar-image-vulnerability/)关于 NGS 软件研究人员开发的 GIFAR 攻击的视角。正如他所解释的，攻击背后的想法，基本上依赖于将一个 JAR 与其他文件相结合，并不新鲜。将 JAR/ZIP 文件与 GIF/JPG 文件组合将创建混合文件，文件的顶部和底部都有标题，并允许它们作为有效文件绕过任何图像处理库。虽然加强安全性和更严格的文件验证实践是可取的，但问题不仅仅是浏览器安全中的漏洞。ZIP 是一种无处不在的通用打包技术，从 Microsoft 文件到打开的 Office 文档，当然还有 JAR 文件。他最后说，“任何基于 ZIP 的文件格式，只要你允许你的用户上传到你的服务器上，都可能被用于攻击”

[图片:[乔恩·雅各布森](http://flickr.com/photos/loganart/2717705743/)

*   [永久链接](http://www.gnucitizen.org/blog/more-on-gifars-and-other-dangerous-attacks/)