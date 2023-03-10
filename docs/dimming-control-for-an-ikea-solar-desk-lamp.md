# 宜家太阳能台灯的调光控制

> 原文：<https://hackaday.com/2011/05/16/dimming-control-for-an-ikea-solar-desk-lamp/>

[弗兰克]决定增加他的台灯的功能，增加调光控制 ( [翻译](http://translate.google.com/translate?js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&sl=auto&tl=en&u=http%3A%2F%2Fwiki.villaro-dixon.eu%2Fdoku.php%3Fid%3Delectronique%3Alampe_ikea%3Aaccueil))。由于光源是由三个发光二极管组成的，因此降低其亮度的最佳方法是使用脉冲宽度调制。这就是他采用的方法，幸运的是，他作为项目捐赠人使用的宜家孙楠[灯刚好有足够的空间来容纳这次改装所需的部件。](http://www.ikea.com/us/en/catalog/products/90154371)

你需要两个主要位来使用这样的灯的 PWM 微控制器(或者可能是定时器芯片，如 555)和晶体管，以保护该芯片免受使 led 以全亮度运行所需的电流。[Frank]选择了一个 ATtiny13 和一个 2N2222 晶体管，这两个晶体管都很常见，而且非常便宜(如果你知道在哪里可以找到，你甚至可以从一个灯泡中取出微控制器)。灯座的顶部增加了两个按钮，可以上下控制。甚至还有一个 SOS 功能，同时按下两个按钮就可以触发。[Frank's]休息后，高兴地在剪辑中展示已完成的项目。

[https://www.youtube.com/embed/lyg1QQ1XCvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/lyg1QQ1XCvo?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)