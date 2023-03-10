# 人工协议分析

> 原文：<https://hackaday.com/2009/01/24/manual-protocol-analysis/>

![packetfu](img/97afa037d11a4181d638551a79962b5d.png "packetfu")

作为上周关于[自动化协议分析](http://hackaday.com/2009/01/13/automated-protocol-analysis/ "Automated protocol analysis  - Hack a Day")的帖子的后续，【托德·比尔兹利】写了如何开始[手动分析协议](http://www.breakingpointsystems.com/community/blog/manual-protocol-reverse-engineering)。他通过几个例子展示了如何提取二进制协议中有趣的部分。他的第一步是发送 10 条相同的 select 语句并捕获出站数据包。他使用 Ruby 库 [PacketFu](http://code.google.com/p/packetfu/) 来帮助识别。它比较了 10 个数据包，并突出显示了每个数据包增加 4 的一个字节，可能是一个计数器。查看响应显示，其他几个字节也以相同的速率增加，但值不同。在两个不同的日子运行相同的查询，结果可能是一个时间戳。使用两个不同的查询有助于确定哪个字节负责语句长度。虽然你可能不会发现自己每天都沉浸在巫术中，但这篇文章很好地介绍了如何批判性地思考这个问题。