# 语音识别地理缓存:西班牙语

> 原文：<https://hackaday.com/2011/03/18/speech-recognition-geocache-se-habla-espanol/>

![](img/15f17eeb03c695f26822bf6444d16889.png "Voice-activated-Geo-Cache (Custom)")

Instructables 用户[jorgegunn]在最近的 geocache 版本上加入了语音识别功能，并要求“发现者”知道秘密密码才能访问里面的战利品。虽然我们不会破坏这里的乐趣，但通过选择适合任何徒步旅行者的密码，该版本的技术精神得到了进一步加强。

尽管使用了现成的语音识别电路套件，但这种攻击的大部分是使用当地电子和五金店提供的零件完成的。[jorgegunn]不遗余力地让任何业余爱好者都可以访问这个黑客，甚至包括相关教程、原理图和在线零件供应商的链接。

实际的语音识别是通过一个 [Images Scientific Instruments 型号 SR-06 电路套件](http://www.imagesco.com/kits/speech-recognition-kit.html "Images Scientific Instruments SR-06")完成的，能够识别多种语言中多达 40 个不同的预定义单词。每当出现正确匹配时，一个与该单词的存储槽相对应的值就会显示在一对 7 段显示器上。基于 74LS373 D 型锁存器和 4028 IC 解码器 CMOS 的独立解码器电路确定正在显示的值是否构成有效响应，然后通过达林顿晶体管驱动螺线管，以释放闭锁机构。一旦打开，该设备只是被推回关闭，以等待下一个发现者-我们猜测，从它的大小来看，找到它可能是最容易的部分！

虽然现实世界的电池寿命尚未确定，但用于记忆保持的单个硬币电池和用于驱动电路和锁存释放的 9V 电池持续了整整一个月的测试，没有出现任何问题。通过简单的太阳能电池和可充电电池设置，电池寿命几乎可以无限延长，但这也明显增加了破坏和/或盗窃的可能性。

我们可以想象这种设备的许多不同的应用，包括自动门锁机制，甚至是对诸如计算机机箱上的控制之类的东西的访问控制。通过将多个单词串成一个密码，或者在一定次数的错误猜测后设置一个“超时”时间，也应该很容易增加安全性。

请在下面的评论中告诉我们任何其他应用程序或构建变体，并确保在休息后的短视频中看到它们是如何组合在一起的。

[https://www.youtube.com/embed/QqPVJqzKb3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/QqPVJqzKb3E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent) [https://www.youtube.com/embed/OvRFG1-tQHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/OvRFG1-tQHY?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)