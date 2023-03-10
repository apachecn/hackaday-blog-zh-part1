# 使用旋转式数字键盘会降低生产率

> 原文：<https://hackaday.com/2010/02/26/lower-productivity-by-using-a-rotary-num-pad/>

[https://player.vimeo.com/video/9618204](https://player.vimeo.com/video/9618204)

[Maximilian Ernestus]给了我们一个快速的小演示，展示了他使用[一个旋转式电话拨号盘作为数字键盘](http://translate.google.com/translate?js=y&prev=_t&hl=en&ie=UTF-8&layout=1&eotf=1&u=http%3A%2F%2Ferniejunior.wordpress.com%2F2010%2F02%2F21%2Ftelefon-als-nummernfeld%2F&sl=de&tl=en)。当笔记本和上网本禁止我们使用我们的 mad 10 键技能时，我们经常感到沮丧(备用键映射不算)。这使得在小型便携设备上编码和使用 [GnuCash](http://www.gnucash.org/) 变得不理想。

[Maximilian]没有解决这个问题，而是将一个旋转式电话接口为数字键盘，使问题变得更糟。Arduino 对脉冲进行计数，并通过串行连接将其输入计算机。从那以后，只需要一点软件处理就可以发出一个按键。他提到未来的版本应该注册为 USB 键盘。这是抛弃 Arduino 并使用 [V-USB 库](http://www.obdev.at/products/vusb/index.html)的绝佳机会。

想更深入地了解这项老技术吗？不要错过来自[神奇手机黑客](http://hackaday.com/2005/11/22/the-magic-phone-take-two/)的信息。