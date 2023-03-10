# 在你的 Playstation Portable 上的 Hackaday

> 原文：<https://hackaday.com/2005/03/26/hackaday-on-your-playstation-portable/>

![hackaday psp](img/97bfcd92869200f403186a25e93e6176.png)

新的 psp 游戏 [wipeout pure](http://www.us.playstation.com/games.aspx?id=UCUS-98612) 显然配备了一个全功能的网络浏览器，用于下载更新。通常它仅限于这个目的，但是 roto 今天早上给我发了一条消息，说通过一点 dns 欺骗，它可以被黑客攻击，作为一个通用的网络浏览器。

只需将 psp 指向一个你可以控制的域名服务器，为 ingame.scea.com 创建一个 dns 入口，让它进入你自己的网络服务器，然后在那里粘贴一个/wipeout/index.html。当你点击 wipeout 中的下载，它将加载你的自定义页面！

我被告知浏览器支持 javascript，所以编写一个快速地址栏，并链接到谷歌，以及(当然)你最喜欢的网站。

(感谢雅皮士链接到[工作镜](http://www.fumanchuu.com/pspdev/)。[作者的网址在这里](http://mozy.org/psp/)，但目前已关闭。)

**更新**:刚从 roto 收到一些更详细的信息。继续阅读了解更多信息。

**来自罗托的邮件:**

> 以下是我所做的总结(摘自论坛帖子):
> 
> Wipeout Pure for PSP 有一个特性，可以让你在线访问更新的内容(比如抓取新的纹理或者关卡)。这个小小的特征被颠倒过来，并为我们所用。注意，我不是第一个这样做的人，我也从未声称自己是。不过，我确实自己发现了这一点(你可以在论坛帖子上找到其他 4 个人的链接)。
> 
> 无论如何，进入勇敢向前冲的“下载”部分，我们会看到一个隐藏的但功能齐全的网络浏览器，这个浏览器现在被 SCEA 的网络服务器上的“即将推出”的标志遮住了。
> 
> 把访问请求分开，我发现(像许多其他人一样)这可以通过简单的“欺骗”来利用
> 
> 我加载我自己的“页面”的方式是通过用一些 DNS 条目设置我的 FreeBSD 机器，这些条目将 ingame.scea.com 和 webcluster.scea.com 以及 scea.com 的所有 NS 指向我的内部局域网机器。我还为 Apache 创建了一些文件。于是我改变了 PSP 的名称服务器设置，指向我本地局域网上的服务器(FreeBSD 机器)。由于 DNS 映射，当勇敢向前冲客户端访问 http://ingame.scea.com/wipeout/index.html 时，它会获得我的本地文件。之后就很简单了。我做了一个静态页面，上面有一堆 spring-board(我猜是门户类的)链接，可以从 PSP 上访问。当您通过按“开始”选择“转到主页”时，将返回到门户网站(index.html)。所以这是一个简单的方法。
> 
> 浏览的时候，你可以输入输入(我们 googled 了东西！)，当你输入一个文本框并按下 X 键时，PSP 会弹出键盘 API(记住有很多 API 可以被 PSP 利用)。之后，它就像 PSP 上的任何其他输入一样简单。
> 
> 浏览很简单，上下移动就可以从一个链接到另一个链接。不过只能用 D-Pad。也没有光标，也没有标题栏。如果最近的附近没有链接，PSP 只是滚动页面(牛逼)。进入链接是 X，刷新页面是[]。再次在文本框中输入文本会弹出 API。
> 
> JavaScript 起作用了(又是警告框的 API，简洁的特性…我的朋友 MomDad 用一句“恐慌！”吓了我一跳笑话原来是 PSP 的对话框 API 踢进来)，Java 还有待测试。框架不起作用。大图片也要测试。嗯，我想现在就这样了。大部分 HTML 作品(没有 H1 的东西)。背景颜色和图片等工作良好。
> 
> 我为你附上一张巨大的黑客照片:)喜欢你的网站。

啊，呸。谢谢罗托！

*   [永久链接](http://mozy.org/psp/)