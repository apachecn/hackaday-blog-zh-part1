# 磁条卡欺骗器

> 原文：<https://hackaday.com/2008/08/04/magnetic-stripe-card-spoofer/>

在制造了一个 USB 磁条阅读器之后，大卫·克兰诺尔发现了一种利用手动缠绕电磁铁和 iPod 来欺骗磁条阅读器的方法。卡上的数据被读取并存储在计算机上，然后用 C++程序编码成 WAV 文件。iPod 通过连接到耳机插孔的单级运算放大器播放 WAV 文件和数据。放大器用来驱动电磁铁。跳跃后嵌入的视频。

这绝不是一个新想法。出现了很多[磁条项目](http://deepquest.code511.com/blog/more.php?id=263_0_1_0_M)和[软件](http://stripesnoop.sourceforge.net/hardware/reader.html)。这个项目特别引用了 1992 年由[Count Zero]撰写的 Phrack 文章“[通量逆转的一天](http://www.phrack.org/issues.html?issue=37&id=6#article)”。

Don’t get your hopes up just yet on strolling through high security installations using this little device. It can only replay the data from a card that has been recorded. If you don’t have a known working card, it won’t get you very far.

[via [Hackszine](http://www.hackszine.com/blog/archive/2008/08/magnetic_stripe_card_spoofer.html)

*   [永久链接](http://www.instructables.com/id/Magnetic_stripe_card_spoofer/)