# 现代怪异:从 YouTube 音频中提取电话号码

> 原文：<https://hackaday.com/2011/02/13/modern-freaking-pull-phone-numbers-from-youtube-audio/>

![](img/0e7f31a3bfeabff7e33692f5ec10c4f5.png "sniffing-telephone-numbers-from-audio")

[查理 X 射线]正在用电话系统玩一些现代的乐趣，通过从 YouTube 视频的音频轨道中提取拨号号码。第一步是找到一段视频，视频中电话正在被拨打*和*按键的声音是可以听到的。你不能区分这些音调，但是电脑可以。这是因为每按下一个数字，就会产生七分之二密切相关的频率组合。[Charlie]使用 Audacity 分离音频，然后编写 python 脚本来生成如上图所示的声谱图。通过匹配两个暗节点，你可以确定播放了哪两个频率，并解码正在拨打的电话号码。那么这又是如何工作的呢…找到被拨电话的音频，解码号码..利润？