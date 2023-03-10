# 改造挡风玻璃雨刷，使其与音乐同步

> 原文：<https://hackaday.com/2012/03/10/over-engineering-windshield-wipers-to-sync-to-music/>

![](img/3c637acc68dd6a5cbdf5c7588c526157.png "Achievement")

90 年代末，大众播出了一系列精彩的电视广告，赢得了一些与广告界相关的奖项。其中一个广告的标题是 *[同步](http://www.youtube.com/watch?feature=player_embedded&v=DcfW_hlYZ5k)* ，展示了一辆大众捷达的挡风玻璃雨刷(以及其他东西)随着音乐同步行驶在一条下雨的小巷中。[ch00f]认为 [beat tracking 雨刷](http://ch00ftech.com/2012/01/22/beat-tracking-windshield-wipers/)将成为一个伟大的项目，我们喜欢投入到这个构建中的大量工程。

建造开始于[ch00f]拆开他的雨刷马达，为他的建造获得一些细节。理想情况下，旋转编码器对这个项目非常有用，但设计一个耐用的编码器无论如何都是一件痛苦的事情。[ch00f]必须解决刮水器齿轮电机上的“止动销”问题，以允许刮水器以间歇模式驱动。

[ch00f]花了大量时间编写代码来保证恒定的雨刷速度，但这并没有解决相位问题，或者让雨刷在节拍上开始或结束它们的周期。通过使用前馈系统，这个问题在某种程度上得到了解决(正如你在休息后的视频中看到的)——基本上，软件会预测所需的相位变化，并通过改变速度来纠正它。

虽然这主要是因为雨刷马达上的雨刷停止开关的位置，但是这个版本仍然不完美。[ch00f]计划花多一点时间用软件修正雨刷速度/相位控制，但他现在得到的仍然非常令人印象深刻。

[https://www.youtube.com/embed/kOCpIA_D6nU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/kOCpIA_D6nU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)