# 向钥匙卡锁添加小键盘

> 原文：<https://hackaday.com/2009/10/09/adding-a-keypad-to-a-key-card-lock/>

![keypad](img/bc2f0102264994444b84383ac32fcbbe.png "keypad")

[科林·默克尔]有一个小问题:他总是忘记带电子钥匙卡，把自己锁在宿舍外面。像任何一个普通的黑客读者一样，与其养成总是带着名片的习惯，自然的冲动当然是[建造这个由电子设备和胶带](http://www.instructables.com/id/An-Electronic-Door-Opener/)组成的精致装备。对吗？

其结果是一个额外的键盘，可以用来获得访问…不改变现有的电子锁，但与第二个机制，操作内门把手。一个 8 位 [PIC](http://hackaday.com/2009/09/12/controlling-an-rc-car-with-a-pic16f84/) 微控制器扫描外部[键盘](http://hackaday.com/2009/09/18/touch-sensitive-keypad/)(通过一根细带状电缆连接)，当输入正确的访问代码时，启动 12 伏 DC 电机转动手柄。这是一篇很棒的小文章，包括部件列表、源代码，并解释了键盘扫描的过程。

这类似于我们之前发布的基于 RFID 的宿舍黑客攻击。通过物理操作手柄，几乎任何方法都可以使用:[面部识别](http://hackaday.com/2009/04/30/face-tracking-in-opera/)，其他[生物识别](http://hackaday.com/2008/08/15/biometric-locks-turned-trojan/)， [DDR pad](http://hackaday.com/2007/05/03/laser-dance-pad/) ，或者任何你能想到的灵感来源。