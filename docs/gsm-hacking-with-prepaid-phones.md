# 预付费手机的 GSM 黑客攻击

> 原文：<https://hackaday.com/2010/12/30/gsm-hacking-with-prepaid-phones/>

想监听手机通话或拦截测试信息吗？这侵犯了别人的隐私，你真可耻！但是有黑帽子想这么做，这可能没有你想象的那么难。[这篇文章总结了一种方法](http://arstechnica.com/gadgets/news/2010/12/15-phone-3-minutes-all-thats-needed-to-eavesdrop-on-gsm-call.ars)使用预付费手机和一些解密技术来快速获取手机上的所有通信。[Karsten Nohl]和[Sylvain Munaut]在混沌通信大会上演讲的幻灯片现在可以在[获得](http://events.ccc.de/congress/2010/Fahrplan/events/4208.en.html)，但要点如下。他们用定制固件刷新了一些廉价手机，以获取所有通过网络传输的数据。通过发送精心制作的幽灵消息，目标用户不会收到收到文本的通知，但手机确实在与网络通信。该流量用于嗅出大致位置，并最终获取会话密钥。该密钥可用于抽取所有网络通信，然后通过使用 1 TB 的彩虹表快速解密。这不是一个简单的过程，但这比我们想象的要简单得多。

[谢谢罗伯]