# DNS 缓存中毒网络广播

> 原文：<https://hackaday.com/2008/07/24/dns-cache-poisoning-webcast/>

![](img/f8dee406dbb04ca6734cf4aee9e631fa.png)
**更新:** [网络直播的完整音频现已发布](http://blackhat.com/html/webinars/kaminsky-DNS.html)

今天[黑帽](http://www.blackhat.com/)与【丹·卡明斯基】就他发现的大量 DNS 漏洞举行了一次网络直播预览。7 月 8 日，多家厂商[宣布了一个针对未披露的 DNS 漏洞](http://www.hackaday.com/2008/07/08/major-dns-issue-causes-multivendor-patch-day/)的补丁。[Dan Kaminisky]当时没有公布漏洞的细节，但鼓励安全研究人员不要公布他们的工作，如果他们碰巧发现了这个漏洞。21 日，[漏洞的完整描述被泄露](http://blog.wired.com/27bstroke6/2008/07/details-of-dns.html)。

在今天的网络广播中，[Dan]谈到了他对漏洞处理的看法，并回答了一些相关问题。他首先讲述了自己是如何偶然发现这个 bug 的；他正在研究如何通过使用 DNS 找到离客户端最近的服务器来加快内容分发。这种新的攻击之所以有效，是因为不使用端口随机化的 DNS 服务器使得攻击者很容易伪造响应。你可以在这里阅读攻击的细节。

[Dan]谈到了自 7 月 8 日公告以来所做的工作。少数研究人员联系了他，手上拿着确切的 bug，但按照要求，没有公布信息。当第一次宣布时，在 doxpara.com 上使用 checker 自愿测试的所有服务器中有 86%是易受攻击的。13 天后，该漏洞被公布，只有 52%的使用 checker 的人易受攻击。这并不完美，但 13 天给了很多公司足够的时间来测试和推出他们的补丁。

[Jerry Dixon]美国国家网络安全部门前主任指出，即使漏洞最终被泄露，补丁也已经出了 13 天；这不是一个没有补丁的零日漏洞。所以，我们处于相当有利的位置。也就是说，自从我们昨天[发布 Metasploit】以来，他们已经推出了新的模块代码，将](http://www.hackaday.com/2008/07/23/dns-exploit-in-the-wild/)[接管整个域](http://www.caughq.org/exploits/CAU-EX-2008-0003.txt)。安全研究员[Rich Mogull]认为快速产生这种利用代码是“[扯淡](http://twitter.com/rmogull/statuses/867475896)”和“[只帮助坏人](http://twitter.com/rmogull/statuses/867476311)”。

[Dan]指出，人们已经做了一些相关的工作，使用防火墙来减轻 DNS 缓存中毒。[Michael Rash]写了关于在 Linux 中使用 iptables 随机化出站请求的文章，[Jon Hart]介绍了在 OpenBSD 中使用 PF 的情况。该团队正在积极联系易受攻击的服务器，让他们打补丁。他们还建议 IDS 供应商寻找具有相同 ID 的多个回复，作为这种攻击的迹象。

你可以使用[doxpara.com](http://www.doxpara.com/)上的工具检查你的 DNS 服务器。我们亲自将我们的机器切换到 208.67.222.222 和 208.67.220.220 的 [OpenDNS](https://www.opendns.com/) 服务器上。它不仅给了我们一些想法，而且性能比我们的 ISP 过载的 DNS 好得多。