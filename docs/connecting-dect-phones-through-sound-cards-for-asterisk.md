# 通过星号的声卡连接 DECT 电话

> 原文：<https://hackaday.com/2005/10/08/connecting-dect-phones-through-sound-cards-for-asterisk/>

![board](img/acf43477f9e7de6f3f80e006dd64c34f.png)

我想不出更好的标题了。事情是这样的:[onno]想要[将一部 DECT 手机转换成 VOIP 使用](http://www.okay.dyndns.org/okhp/linux/asterisk/)。首先，他尝试使用变压器的音频，但不满意的噪音和回声。他描述了如何像[【克里斯多佛】的 Skype 电话](http://www.grynx.com/index.php/projects/siemens-skype/)那样直接窃听，但也包括了防止烧坏你的声卡的所有必要措施。这个项目的主要部分是他为[星号](http://www.asterisk.org/)破解的“chan_oss”驱动程序。使用驱动程序，星号可以拨打 DECT 的电话。它还通过将声音输入与已知的线路噪声水平进行比较来检测电话是否摘机。该电话可以像任何标准电话一样使用 DTMF 拨号。

*   [永久链接](http://www.okay.dyndns.org/okhp/linux/asterisk/)