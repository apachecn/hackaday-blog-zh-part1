# 综述:简单的黑客攻击

> 原文：<https://hackaday.com/2009/11/09/quickhack-ipod-hdd-to-cf-conversion/>

![simple-hack-110909](img/d433a7d889d7fbb3e6be53349c7db78d.png "simple-hack-110909")

这里有一些你可以在大型项目之间使用的简单技巧。休息之后，我们将看看如何将 iPod 从硬盘存储转换为紧凑型闪存，使用乐高和 USB 电源建立一个 LED 台灯进行充电，并使用 Arduino shield 添加一个按钮即可控制网络。

**iPod HDD 到 CF 的转换**

![ipod-hdd-cf-conversion](img/affb0b12a3eaf5c6ffc4ec50e2f29cb2.png "ipod-hdd-cf-conversion")

[Richard]向我们透露了关于将 iPod 从硬盘转换成闪存卡的消息。我们几年前就这样做了。因为我们经常购买坏掉的电子产品，我们有一个旧的 20GB 的 iPod 和一个坏掉的硬盘。知道我们已经看到了[的一个有线色情类型的 diy 适配器](http://geektechnique.org/projectlab/767/put-flash-memory-into-almost-any-ipod)和[报道的另一个](http://hackaday.com/2006/10/04/ipod-hd-adapter/)，快速搜索产生了一个现成的解决方案。

[Richard]走了同样的路，购买了一个 CF 转 1.8 英寸 IDE 适配器和一个 32GB 的闪存卡。只要打开你的 iPod，拔掉坏了的硬盘，插上适配器和 CF 卡，合上外壳，然后经历一个正常的 iPod 恢复周期。紧凑型闪存比固态硬盘便宜得多，这使得这种转换比类似的 Zune 升级更便宜。

你瞧，曾经破碎的现在完整了。

**LED 乐高灯**

**![LEGO-lamp](img/4e95135feb988ee617685cbb9e03dc58.png "LEGO-lamp")
**

用他手头的零件组装了一盏台灯。开关、电池和 USB 充电功能使用了损坏的蓝牙耳机。在那里，他用乐高建造了一个关节臂和身体。提供照明的最后一步只是连接一个白色 LED。这不是[最漂亮的 LED 灯](http://hackaday.com/2009/10/22/unreasonably-bright-bike-light-apparently-hunts-deer/)，但它完成了任务，并为你的办公桌增添了一点“这是我造的”的骄傲。

**通过网络连接的静音按钮**

**![arduion-ethernet-solution](img/e142f7c576466ddf7bfe3125ae42c91b.png "arduion-ethernet-solution")**

[Justin]房间另一端的一些扬声器需要静音按钮。音乐是由 Mac mini 播放的，所以他制作了一个静音按钮，可以通过网络发送命令。通过为 Arduino 使用以太网屏蔽，他能够检测到按钮按下，并通过 XML-RPC 服务器发送命令，以获得一些和平和安静。该设备通过以太网供电。[以太网屏蔽是我们最喜欢的附加组件之一](http://hackaday.com/2008/11/06/official-arduino-ethernet-shield/)，承担着连接工作的主要任务。

不要害怕[发送各种难度的黑客](http://hackaday.com/contact-hack-a-day/)。如果你有一个简单一点的，我们可以把它作为一个群体的一部分。