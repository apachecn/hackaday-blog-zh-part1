# RFID 门锁——正确的方法

> 原文：<https://hackaday.com/2009/11/17/rfid-door-lock-the-right-way/>

[https://www.youtube.com/embed/XT7E_GEIPVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/XT7E_GEIPVg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[Pcmofo]分享了一个关于如何为门实现 RFID 钥匙系统的构建良好、解释清楚的示例[。我们称之为正确的方法，因为它是经过深思熟虑的，并且是实用的。过去我们见过通过秘密敲门](http://www.instructables.com/id/Arduino-RFID-Door-Lock/)、[键盘](http://hackaday.com/2009/10/09/adding-a-keypad-to-a-key-card-lock/)和 [RFID](http://hackaday.com/2009/01/02/rfid-dorm-room-door/) 解锁[的门，但它们都是能够从一扇门移植到另一扇门的非永久性解决方案。这种实现不是建立一种转动门把手的机制，而是使用安装在门框上的电闸来允许进入。这些是用于建筑物的安全门，是为了保证你的门的安全而建造的。](http://hackaday.com/2009/11/04/knock-detecting-lock/)

在这种情况下，黑客是电子设备。使用运行 Arduino 引导加载程序的 AVR ATmega168，[pcmofo]已经原型化了两部分设计。RFID 阅读器安装在门外，数据线连接到微控制器所在的内部。硬编码 RFID 卡被用作“主”来训练任何数量的标签用于进入。主人将设备置于训练模式，下一个要读取的标签被添加到被授权开门的标签列表中。

我们喜欢杂乱的电线和快速组装在一起的设备，但这是为了持久而建造的，一旦安装在适当的外壳中，就会看起来很棒。