# 新的 WPA TKIP 攻击

> 原文：<https://hackaday.com/2008/11/09/new-wpa-tkip-attack/>

![wifibox](img/f88f9fd127787ff139cfe17a89934014.png "wifibox")

[Martin Beck]和[Erik Tews]刚刚发布了一篇论文，内容涉及针对 WEP 的改进攻击和针对 WPA 的全新攻击。对于 WEP 的一半，他们提供了一个很好的攻击概述到这一点，以及他们所做的优化，以减少所需的数据包数量约为 25K。到目前为止，WPA 面临的唯一严重威胁是 [coWPAtty](http://wirelessdefence.org/Contents/coWPAttyMain.htm "coWPAtty Main Page") dictionary 攻击。这种新的攻击允许您解密 WPA 数据包明文的最后 12 个字节，然后生成任意数据包发送给客户端。虽然它不能恢复 WPA 密钥，但攻击者仍然能够直接向他们攻击的机器发送数据包，并可能通过到互联网的出站连接读回响应。

[照片:尼亚美

[途径〔t1〕无〔t1〕