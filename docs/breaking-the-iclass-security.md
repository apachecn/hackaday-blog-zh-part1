# 破坏 IClass 安全性

> 原文：<https://hackaday.com/2011/02/23/breaking-the-iclass-security/>

![](img/40217a9b2e0e2606ee520f5025490d4d.png "cracking-iclass-rfid")

iClass 是支持 RFID 的门禁卡的一种流行格式。这些卡发给公司员工，允许他们通过每个安全门的读卡器进入大楼的各个部分。我们早就知道，这些访问系统在安全性方面相当薄弱。但是现在你可以发现他们是多么的脆弱，安全是如何被破解的。[Milosch Meriac]深入研究了 HID iClass 设备的安全协议，并在一份白皮书中列出了细节。

该过程中最具侵入性的部分是破坏 PIC 18F 系列芯片的复制保护，以读取控制读卡器的固件。这是通过 USB 转串行电缆和软件实现的，该软件对 ICSP 协议的实现进行了位碰撞。在擦除和攻击了几个芯片(一次一个数据块)后，原始代码被读出并拼凑在一起。休息之后，请查看[Milosch]在 27C3 embedded 的演讲，并从白皮书中获取 ICSP 比特碰撞攻击的代码。

[https://www.youtube.com/embed/mZNSYw9oH4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/mZNSYw9oH4Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)