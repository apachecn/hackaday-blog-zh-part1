# 逆向工程你的 BIOS

> 原文：<https://hackaday.com/2006/05/21/reverse-engineer-your-bios/>

![wooden laptop](img/9324e559f164ed81da31bca89791a46d.png)

[th0mas]有一个有趣的指南，教你如何在 BIOS 中修改引导镜像。这很容易损坏你的笔记本电脑，但是看看它是怎么做到的很有趣。他首先转储纯文本字符串。位图格式的幻数出现在文件中，因此他从该点开始复制了一大块数据。th0mas 在 MSPaint 中打开这个来保持格式。在修改图像后，它被放回 BIOS 文件中，并执行几项检查以确保只有图像数据发生了变化。最后一部分涉及在调试器中运行 flash 实用程序，以找到检查 CRC 的位置。通过修改程序，他可以在程序没有抱怨的情况下刷新图像。

*   [永久链接](http://os-fun.blogspot.com/2006/05/modifying-laptop-bios-for-fun-and.html)