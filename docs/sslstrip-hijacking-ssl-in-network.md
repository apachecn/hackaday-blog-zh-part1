# Sslstrip，劫持网络中的 SSL

> 原文：<https://hackaday.com/2009/02/23/sslstrip-hijacking-ssl-in-network/>

上周在黑帽 DC 大会上，[莫邪·马林斯派克]展示了一种劫持 SSL 的新方法。你可以在这篇[福布斯文章](http://www.forbes.com/2009/02/18/black-hat-hackers-technology-security_0218_blackhat.html "Breaking Your Browser's 'Padlock' - Forbes.com")中读到，但我们强烈建议你观看视频。 [sslstrip](http://www.thoughtcrime.org/software/sslstrip/index.html) 可以将所有 https 链接重写为 http，但远不止于此。使用看起来像/和的 unicode 字符？它可以用有效的证书构造 URL，然后在窃取用户的凭据后将用户重定向到原始站点。即使是普通用户也很难注意到这种攻击。这种攻击需要访问客户端的网络，但是[莫邪]在一个 [Tor](http://hackaday.com/tag/tor/ "tor  - Hack a Day") 出口节点上成功地运行了这种攻击。