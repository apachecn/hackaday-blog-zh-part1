# 重置激光打印机的页数

> 原文：<https://hackaday.com/2012/03/05/resetting-the-page-count-on-a-laser-printer/>

[Brian]真的很喜欢他的三星彩色激光打印机，直到该换墨盒的时候。一整套碳粉盒的售价与打印机本身的价格差不多，所以[Brian]认为他可以简单地将碳粉补充到他现有的碳粉盒中。打印机会根据页数发出“碳粉不足”警告，如果页数过多，打印机将无法打印，从而降低了碳粉补充套件的经济性。幸运的是，[Brian]想出了一个非常简单的方法来重置页数，这样他就可以使用那些第三方填充套件了。

打印机的所有配置设置和页数都存储在 I2C EEPROM 中。在用 Arduino 转储 EEPROM 上的数据，用总线盗版嗅探所有进入 EEPROM 的数据后，[Brian]几乎智穷才尽。谢天谢地，幸运之神介入了。当[Brian]重新启动连接了总线盗版的打印机时，他注意到初始化时间要长得多。打印配置报告时，他惊恐地发现所有页面计数都已归零。

允许[Brian]重置页数和使用过的重新填充的碳粉盒的最后一个方法是在启动时将 EEPROM 的 SDA 线接地的简单导线。[Brian]使用了一个瞬时开关，但是考虑到这是每几个月一次的操作，一根简单的电线就足够了。休息之后看看[Brian]的页面重置演示。

[https://www.youtube.com/embed/077GLsEMV2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/077GLsEMV2E?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)