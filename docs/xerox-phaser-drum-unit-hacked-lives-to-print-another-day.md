# 施乐移相器鼓单元被黑，生活打印另一天

> 原文：<https://hackaday.com/2011/04/18/xerox-phaser-drum-unit-hacked-lives-to-print-another-day/>

![](img/27b47752716a2e3c954a9a88965c163c.png)

面对一台无缘无故停止打印的打印机，芬兰海盗兼黑客[Janne]觉得自己受够了。在做了一点研究后，他[拆卸了滚筒组件并更换了一些部件](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=fi&tl=en&u=http%3A%2F%2Fusvi.puheenvuoro.uusisuomi.fi%2F69162-suuri-hehkulamppuhuijaus-nain-selatetaan-xerox)。最终结果？据说“坏了”的打印机又开始工作了。

显然，施乐公司使用一个相当基本的方案来决定什么时候该更换你的打印机硒鼓了:一个 I2C eeprom 记录打印的页数。在某个数字之后，打印机决定它坏了，不会再打印了。要解决这个问题，需要找到合适的替换内存芯片。最初的芯片是 ST22C02WP。然而，这是很难找到的，所以更换零件被选为 CSI 24C01WI。有趣的是，替换部分只有原始芯片的一半空间，但这似乎并没有造成问题。芯片被调换，经过一些精确的焊接后，打印机被完全修复了。空白替换芯片正常工作…因为打印机和硒鼓之间没有安全或加密措施(得分！)

你是否曾经为了让你的打印机正常工作而不得不与烙铁亲密接触？请在评论中告诉我们。