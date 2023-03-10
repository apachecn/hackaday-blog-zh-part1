# 忍者网络党徽章

> 原文：<https://hackaday.com/2009/08/10/ninja-networks-party-badge/>

![ninjabadge](img/a8344929d920a042cb470ba5fd1bc51d.png "ninjabadge")

**更新:** [导演剪辑的故事](https://forum.defcon.org/showthread.php?t=10787)

虽然官方 Defcon 徽章的报道相当多，但有一个徽章更具排他性，也更受关注。在过去十年的 Defcon 大会上，一群被称为[忍者网络](http://ninjas.org/)的黑客为选定的与会者举办了一场只有受邀才能参加的派对。对于 2009 年的活动，[cstone]和[w0z]制作了一个电子徽章，作为派对的入场券。该徽章基于 8 位飞思卡尔微控制器(MC9S08QE8)，驱动 10 个独立的 16 段 HIOX 格式 LED 显示器。

定制的 pcb 由 4pcb 制造，但所有其他组装都是由波士顿、洛杉矶和拉斯维加斯的一个庞大的志愿者团队手工完成的。这项工作的集会场地由 [Redwire](http://www.redwirellc.com/) 和天使谷媒体提供。创建了 500 多个徽章。为了帮助筹集资金，忍者们聘请了互联网隐私公司 [XeroBank](https://xerobank.com/) 作为活动赞助商。

下面的视频详细介绍了组装过程，其中重点介绍了一些有趣的 DIY 技术，包括使用 30 美元的 Target 热板作为回流炉。

[https://player.vimeo.com/video/5981950](https://player.vimeo.com/video/5981950)

一旦组装好，徽章的默认模式是随机循环显示锁定每个徽章的角色列表，最终显示“忍者党”，与电影“WarGames”中看到的方式相同。徽章还具有“西蒙”游戏模式，能够查看徽章的唯一标识符和赞助商 URL，以及全功能调试器。

使用调试器，用户可以重新编程徽章，以显示不同的信息，或改变它的功能，而不需要计算机。下面的视频演示了这一点。

[https://www.youtube.com/embed/K3TY38k0PA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/K3TY38k0PA8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

虽然所有的徽章都在 Defcon 17 上分发，但[cstone]已经提供了[原理图和 gerbers](http://blog.mahalo.com/hackaday/ninjabadge/defcon-ninja-docs.zip) ，公共域[源代码](http://blog.mahalo.com/hackaday/ninjabadge/proj-20090804213522.tar.gz)，以及 [BOM](http://blog.mahalo.com/hackaday/ninjabadge/dc17-ninjabadge-bom.ods) ，以防你希望创建自己的徽章。我们是帮助手工组装这些徽章的许多人中的一部分，你可以在他的网站上找到列出的。

[照片:[明智](http://www.flickr.com/photos/vissago/3785911437/)