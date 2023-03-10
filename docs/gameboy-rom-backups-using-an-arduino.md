# 使用 Arduino 的 Gameboy ROM 备份

> 原文：<https://hackaday.com/2011/03/20/gameboy-rom-backups-using-an-arduino/>

![gameboy_cart_reader](img/840cafa4ed1fcac9fbcd630919399871.png "gameboy_cart_reader")

[亚历克斯]收集复古游戏机。有一天，当他在玩 SNES 锦标赛时，当他关闭系统时，他保存的游戏被删除了。原来是游戏卡里的电池不知怎么断开了，这让他开始思考。他决定，他想找到一种方法来备份他的保存游戏，从磁带安全保管。

虽然 cart 阅读器存在，但他说现在很难找到，所以他决定使用 Arduino 构建自己的阅读器。SNES 墨盒相对复杂，所以他选择暂时专注于 Gameboy 墨盒。在尝试备份保存游戏之前，他首先选择通过阅读 ROM 来学习如何与盒式磁带[进行通信。](http://www.insidegadgets.com/2011/03/19/gbcartread-arduino-based-gameboy-cart-reader-%E2%80%93-part-1-read-the-rom/)

他详细分解了这些墨盒，讨论了它们是如何构造的，以及如何使用 Arduino 对它们进行寻址和读取。他最终获得了成功，并在他的网站上提供了代码和原理图，供有兴趣的人参考。我们设想保存游戏阅读(也许还有编辑)可能会在不久的将来发生。

看看下面的视频，看看他的购物车阅读器在运行。

[https://www.youtube.com/embed/7u8_dlGbvoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/7u8_dlGbvoA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)