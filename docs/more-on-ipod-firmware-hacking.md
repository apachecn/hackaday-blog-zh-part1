# 关于 Ipod 固件黑客的更多信息

> 原文：<https://hackaday.com/2004/12/11/more-on-ipod-firmware-hacking/>

![ipod hack](img/a9791f6867d0d42321ac10b36e4cec71.png)

这里有一个跟进…在 [engadget 评论](http://features.engadget.com/entry/1234000610023097/)上的海报“zsk009”说…

*无需恢复整个 ipod 即可更新 ipod 固件，在运行更新程序之前，请遵循以下步骤:*

在 ipod 上进入 ipod_control>device>sysinfo
并在写字板中打开文件。
找到这行代码:

buildID: 0x03028000 (3.0.2)
visibleBuildID: 0x03028000 (3.0.2)

用一个更小的数字改变一个数字

buildID: 0x03018000 (3.0.1)
visibleBuildID: 0x03018000 (3.0.1)

现在更新程序会认为你的固件版本是 3.0.1，会让你更新而不需要恢复整个系统。

这已经用 3g 和 4g 测试过了，上面的例子是 4g，3g 使用不同的号码，但实际上是一样的，只是减少了号码。它应该也适用于其他 ipods，但我不确定

(ipod_control 文件夹是一个隐藏文件夹)

谢谢！