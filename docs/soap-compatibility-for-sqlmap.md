# SQLmap 的 SOAP 兼容性

> 原文：<https://hackaday.com/2010/06/25/soap-compatibility-for-sqlmap/>

![](img/8b6d7924ecc3e86c38c98ca61b9adabe.png "sqlmap_plus_soap")

[_coreDump]正在使用 SQLmap 进行一些数据库漏洞测试，以自动化该过程。令他沮丧的是，这个包不能使用简单对象访问协议进行测试。面对不得不手动测试所有 SOAP 漏洞的情况，他决定施展一些 Python 魔法并添加支持。他的解决方案允许 SQLmap 0.8 通过修改包中的三个文件来解析来自 SOAP 协议的 XML 数据。如果您自己的安全测试需要这个功能，他提供了 diff 文件。