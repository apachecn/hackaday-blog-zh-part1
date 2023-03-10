# 25C3:黑客用 200 个 PS3 彻底攻破 SSL

> 原文：<https://hackaday.com/2008/12/30/25c3-hackers-completely-break-ssl-using-200-ps3s/>

一个由安全研究人员和学者组成的团队已经破解了互联网技术的一个核心部分。今天，他们在柏林举行的第 25 届混沌通信大会上公开了他们的工作。该团队能够创建一个[流氓认证中心，并使用它来为他们想要的任何站点发布有效的 SSL 证书](http://phreedom.org/research/rogue-ca/ "Creating a rogue CA certificate")。用户将没有他们的 HTTPS 连接正被监控/修改的指示。

由于 MD5 中的缺陷，这种攻击是可能的。MD5 是一种哈希算法；每个唯一的文件都有一个唯一的哈希。2004 年，一组中国研究人员演示了创建两个具有相同 MD5 散列的不同文件。2007 年，另一个团队展示了利用这些碰撞的理论攻击。该团队专注于利用 MD5 签名的 SSL 证书。

第一步是做一些大范围的扫描，看看哪些证书颁发机构(CA)正在颁发 MD5 签名的证书。他们从 Firefox 信任的 ca 收集了 30K 个证书。其中 9K 是 MD5 签名的。其中 97%来自[rapidsl](http://www.rapidssl.com/ "SSL Certificate Free SSL Certificates RapidSSL Certificate Authority")。

选择了目标后，团队需要生成流氓证书来传输签名。他们利用 200 台 Playstation 3s 的处理能力来完成这项工作。对于这项任务，它相当于 8000 个标准 CPU 内核或 2 万美元的 Amazon EC2 时间。这项任务大约需要 1-2 天来计算。棘手的部分是知道将由 RapidSSL 颁发的证书的内容。他们需要预测两个变量:序列号和时间戳。RapidSSL 的序列号都是连续的。通过测试，他们知道 RapidSSL 总是会在订单被确认后六秒钟签名。知道了这两个事实，他们就能够预先生成一个证书，然后购买他们想要的确切的证书。他们会购买证书来提高序列号，然后在他们计算的准确时间购买。

证书被颁发给他们特定的域，但是由于他们控制了内容，他们改变了标志，使自己成为一个中间的证书颁发机构。这给了他们颁发任何证书的权力。所有这些“有效”证书都是用 SHA-1 签名的。

如果你把时钟拨回到 2004 年 8 月之前，你可以[试试他们的现场演示网站](http://i.broke.the.internet.and.all.i.got.was.this.t-shirt.phreedom.org/)。对于这个例子来说，这个时间只是一个安全措施，对于一个没有过期的证书来说也是一样的。有一个[项目网站](http://phreedom.org/research/rogue-ca/ "Creating a rogue CA certificate")和一个比这个更详细的[报道。](http://www.win.tue.nl/hashclash/rogue-ca/ "MD5 considered harmful today")

为了修复这一漏洞，所有的 CA 现在都使用 SHA-1 进行签名，微软和 Firefox 将把该团队的流氓 CA 列入其浏览器产品的黑名单。