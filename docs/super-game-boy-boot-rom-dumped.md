# 超级游戏男孩开机自甩

> 原文：<https://hackaday.com/2009/09/18/super-game-boy-boot-rom-dumped/>

![gameboy_boot_rom_dump_hardware](img/1d2017a3e99b5c24d94bb9fa9ddb359a.png "gameboy_boot_rom_dump_hardware")

[Costis]设法为任天堂超级游戏机转储了一份启动 ROM。这一小段代码(256 字节)在启动时将图形写入显示器，同时将 ROM 加载到游戏卡带上。他能够通过找到设备锁定启动 ROM 的确切点来转储代码。就在这一点接近他超频的设备导致它运行如此之快，它不能写入寄存器锁定位。一旦通过了这个单点安全，他就执行一个代码，将引导 rom 写到一个他能够读取的不同地址。他已经为你准备了一份[垃圾场的副本以及解释](http://www.its.caltech.edu/~costis/sgb_hack/)供你欣赏。

[谢谢安东尼]