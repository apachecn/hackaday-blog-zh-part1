# 条形码渗透器

> 原文：<https://hackaday.com/2010/09/02/barcode-infiltrator/>

每当有人设法揭露日常设备中的漏洞时，我们都喜欢支持他们。Irongeek 的[Adrian]受到启发[利用条形码](http://www.irongeek.com/i.php?page=security/barcode-flashing-led-fuzzer-bruteforcer-injector)作为攻击 POS 数据库的手段。基于《T2》一集中的一个想法，他开始制作一个快速攻击设备，使用 LED 来欺骗通过扫描条形码接收到的信号。通过将 POS 暴露于一系列普通的数据库攻击，包括 [XSS](http://en.wikipedia.org/wiki/Cross-site_scripting) 、 [SQL 注入](http://en.wikipedia.org/wiki/SQL_injection)以及其他通过输入清理容易解决的错误，他已经创建了自动化系统渗透设备的第一个版本。在这种情况下，硬件很简单，但概念令人印象深刻。

有了硬件的解释和源代码的提供，以及一个基本的未净化输入[备忘单](http://www.irongeek.com/xss-sql-injection-fuzzing-barcode-generator.php)，如果想要成为条形码黑客的人觉得必须提供第二版，他们就有了一个很好的起点。

[谢谢罗伯特·w]