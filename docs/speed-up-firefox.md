# 加速火狐浏览器

> 原文：<https://hackaday.com/2004/12/26/speed-up-firefox/>

![speed up firefox](img/baaef78e1fd86d1a4b6fd8e378183871.png)

forevergeek.com 为宽带用户提供了加速 firefox 的有用指南。基本上，在得到隐藏的配置设置后，你设置浏览器请求更多的数据。
 *1。在地址栏中键入“about:config ”,然后按回车键。向下滚动并查找以下条目:*

network . http . piping network . http . proxy . piping network . http . piping . max requests

通常情况下，浏览器一次只会对一个网页发出一个请求。当你启用管道时，它会一次生成几个，这真的加快了页面加载的速度。

2.按如下方式更改条目:

将“网络. http .管道”设置为“真”

将“network . http . proxy . pipeline”设置为“true”

将“network . http . pipeline . max requests”设置为 30 这样的数字。这意味着它将一次发出 30 个请求。

3.最后右键单击任意位置并选择 New-> Integer。将其命名为“nglayout.initialpaint.delay”，并将其值设置为“0”。该值是浏览器在对收到的信息采取行动之前等待的时间。

如果你使用的是宽带连接，你现在加载网页的速度会快得多！

*   [永久链接](http://forevergeek.com/open_source/make_firefox_faster.php)