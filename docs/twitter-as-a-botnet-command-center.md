# Twitter 是僵尸网络的指挥中心

> 原文：<https://hackaday.com/2009/08/26/twitter-as-a-botnet-command-center/>

![twitter_botnet](img/064bc4072166731c8dd8a4f8adaf1562.png "twitter_botnet")

阿伯网络公司的人在浏览推特时发现了一些非常奇怪的事情:一个推特账户似乎在发布胡言乱语。至少，一开始是这样出现的。经过进一步调查，他们发现该配置文件发布了指向 PKZIP 存档的 base64 编码链接。当他们提取内容并解压缩包含的 DLL 和 EXE 文件时，他们发现该帐户正在建立指向恶意软件的链接，这些恶意软件会将用户信息发布回某些 URL。这篇文章也进行了更新，以表明该计划不仅限于 Twitter，还影响到 Jaiku 和 Tumblr 上的用户。看到所有恶意软件并不像我们通常认为的那样[明显，这有点可怕。](http://hackaday.com/2009/01/17/malware-posing-as-changegov/)