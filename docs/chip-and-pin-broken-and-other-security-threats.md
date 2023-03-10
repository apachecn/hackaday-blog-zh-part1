# 芯片和 Pin 损坏和其他安全威胁

> 原文：<https://hackaday.com/2010/02/12/chip-and-pin-broken-and-other-security-threats/>

![](img/9bb2ce2c82cfc9f1953701898ff855e2.png "chip-and-pin-broken")

在芯片和密码系统中发现了另一个漏洞。该漏洞是一种中间人攻击，不需要太多的专业知识就能实现。你可以[观看 BBC 关于这个问题的报道](http://www.bbc.co.uk/blogs/newsnight/susanwatts/2010/02/new_flaws_in_chip_and_pin_syst.html)或者[查看发现漏洞的团队发表的论文](http://www.cl.cam.ac.uk/research/security/banking/nopin/oakland10chipbroken.pdf) (PDF)。被盗卡位于读卡器中，读卡器通过一根小电缆与伪卡相连。当伪卡插入读卡器时，任何 PIN 都可以用来完成交易。原始卡上的芯片通过签名获得销售完成的确认，供应商的读卡器获得 pin 正确的确认。英国的[芯片和密码](http://en.wikipedia.org/wiki/Chip_and_pin)系统看起来是个好主意，但是它也有安全漏洞。这让我们想知道，给系统中的硬件阅读器推出安全补丁有多难。显然，这需要打补丁，但需要技术人员访问每个终端来刷新升级吗？

转到大规模攻击的话题，我们看到了周三 NPR 对詹姆斯·刘易斯的采访，当时他们讨论了日益增长的网络恐怖主义威胁。他认为对美国电网的攻击是目前最大的威胁，并将在未来十年内发生。显然，关闭电网会危及生命，并使事情停滞不前；红绿灯、制冷、供暖等。我们只是很高兴当被问到他是否认为控制系统中已经存在恶意代码时，他认为事实并非如此。

[感谢 Whatsisface 和 Mcinnes]