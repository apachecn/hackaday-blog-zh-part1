# 破解游戏端口外设，与现代电脑兼容

> 原文：<https://hackaday.com/2011/04/03/hacking-game-port-peripherals-to-work-with-modern-pcs/>

![gameport_hack](img/7c26b548094e64082251b46a69b3b3c5.png "gameport_hack")

[Atiti]有一个抓住旧东西不放的坏习惯。有些人把这种行为称为“囤积”，但在这里，我们理解他的痛苦。原来，在他收集的旧电脑外围设备中，他找到了一个他当年用过的 Thrustmaster 一级方程式赛车车轮。根据你买的东西不同，如今模拟赛车轮子的价格会很贵，所以他决定试试能否破解这个过时的控制器，让它和他的新电脑一起工作。

你看，这个轮子的问题在于它使用了一个“游戏端口”连接器来与电脑连接。如果你不记得游戏端口了，去翻出一个旧的 PCI 声卡，在背面看一下。那个 15 针连接器？那是一个游戏端口。Vista 一发布，微软就停止了对游戏端口的支持，所以[Atti]必须想办法让它在他的新电脑上运行。

他的解决方案是 Arduino，用于读取滚轮输出的模拟信号。这些信号被处理并发送到一个并行端口操纵杆模拟器，使他能够在任何支持标准操纵杆的游戏中使用滚轮。

很明显，他可以去商店买一个 u 盘，但是这有什么意思呢？

请继续关注他刷新车轮的视频演示。

[https://www.youtube.com/embed/F9oggKK5w5Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/F9oggKK5w5Y?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)