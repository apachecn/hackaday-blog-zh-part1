# 逆转谷歌的 IPhone 语音搜索

> 原文：<https://hackaday.com/2008/11/18/reversing-googles-iphone-voice-search/>

![](img/3c0291eeb00fc18621c5610246c2c988.png "had iphone")

谷歌最近更新了他们的[谷歌移动应用](http://www.google.com/mobile/apple/app.html "Google Mobile - Google Mobile App")，增加了一些新功能。当你把电话放在耳边时，语音搜索会自动开始收听。只要说出你要找什么，它就会查询谷歌并返回结果。该应用利用了谷歌的语音识别引擎，他们一直在用 [Goog-411](http://www.google.com/goog411/ "Find and connect with local businesses for free from your phone.") 对其进行训练。[Andy Baio]一直在尝试音频转录，并且[很好奇这个新应用在幕后做了什么](http://waxy.org/2008/11/deconstructing_google_mobiles_voice_search_on_the_iphone/ "Deconstructing Google Mobile's Voice Search on the iPhone - Waxy.org")。当数据包穿过他的网络时，他开始嗅探这些数据包。不幸的是，传输的数据包太小了，他几乎可以肯定自己错过了什么。他会感谢任何帮助。部分问题可能是谷歌获得了特殊待遇，以及[使用了未备案的 iPhone SDK 功能](http://spazout.com/google_cheats_independent_iphone_developers_screwed "spazout.com - The place where chris hughes thinks he is really clever")。