# 使用 PktAnon 的数据包跟踪匿名化

> 原文：<https://hackaday.com/2008/07/11/packet-trace-anonymization-with-pktanon/>

如果你是一名网络研究人员或系统管理员，你会知道网络跟踪通常是必要的，但不容易与同事和其他研究人员分享。为了便于使用和处理敏感信息，远程信息处理研究所开发了 [PktAnon，这是一个匿名网络流量的框架](http://www.tm.uka.de/pktanon/index.html)。

它通过使用基于配置文件的方案来工作，该方案支持各种匿名化原语，从而可以轻松地在不同的网络协议和匿名化方法之间切换。可以很容易地添加新的原语，并且在发行版中捆绑了几个预定义的概要文件。这些概要文件都是基于 XML 的。

本质上，网络跟踪有两个主要用途:匿名化用户流量以进行研究，以及匿名化内部使用，从而防止敏感信息的泄露。这是一个相当死板的方案，但是使用概要文件是一个天才之举，使它变得更加容易，更加灵活，结果是更加有用和强大。

[via [陶安全](http://taosecurity.blogspot.com/2008/07/packet-anonymization-with-pktanon.html)
[图片:[波尔特](http://flickr.com/photos/14882701@N00/2255899768/)

*   [永久链接](http://www.tm.uka.de/pktanon/index.html)