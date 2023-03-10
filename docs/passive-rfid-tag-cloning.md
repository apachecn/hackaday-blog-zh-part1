# 无源 RFID 标签克隆

> 原文：<https://hackaday.com/2011/09/30/passive-rfid-tag-cloning/>

这是一个开源的 RFID 克隆设计,大小和标准的 RFID 钥匙卡差不多。它不需要电池来捕捉键码，只需要 RFID 阅读器产生的磁场。休息之后，您可以在视频中看到演示的功能。当克隆体在 RFID 阅读器的范围内移动时，按住底部按钮，微控制器进入学习模式。现在只要举起你想要克隆的卡，当它捕捉到代码时，按钮上方的 LED 就会亮起。现在，该设备将像最初的 RFID 标签一样工作。

这是由[Ramiro]开发的，他也是我们几天前看到的构建了[准系统 RFID 仿真器](http://hackaday.com/2011/09/26/barebones-pic-rfid-tag/)的人。在研究那个故事的时候，我们跳过了这块宝石。他在标签上发布了大量关于 T2 的信息。看起来他没有留下任何 PCB 或套件，但原理图和代码可供下载。你应该查看一下[设计考虑部分](http://t4f.org/en/projects/open-rfid-tag/49)，因为它讨论了当前版本中没有内置的读/写功能。这就是为什么您会在演示视频中使用的硬件上看到一些附加组件。

看起来这比我们上次看的中的【RFID 欺骗器要友好得多。

[https://www.youtube.com/embed/RFWFh6Ko5YE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/RFWFh6Ko5YE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)