# 使用谷歌文档作为网络代理

> 原文：<https://hackaday.com/2012/01/31/using-google-documents-as-a-web-proxy/>

![](img/5582526a9c7f9b89ce4163ad3edd0486.png "google-spreadsheet-as-proxy")

虽然听起来很奇怪，但是有一种方法可以使用谷歌文档作为网络代理。上图是[Antonio]的截图，展示了他如何通过这家网络巨头的云应用程序查看来自任何网站的文本数据。你所在的位置可能会屏蔽某些网站，但大 G 可以加载任何它想要的内容。如果你需要的只是文本，那么你也可以。

黑客利用了 Google 电子表格的=IMPORTDATA()函数。我们猜测这个命令是为了使 XML 数据的导入成为可能，但是，嘿，HTML 数据也差不多是这样，对吗？但是电子表格中的原始网页代码有什么好处呢？这就是[安东尼奥]在把这个放在一起时做出的一个相当聪明的跳跃。他创作了一个 bookmarklet，它提供了一个导航界面，隐藏了存储在 spreasheet 中的原始代码，并将其呈现在浏览器中。这将用户提供的 URL 联系在一起，在隐藏的电子表格上重新加载数据，并根据需要刷新窗口。休息后在片段中自己看吧。

[https://www.youtube.com/embed/hQUTiXmdBUU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hQUTiXmdBUU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)