# 有推特功能的糖果机根据命令分发糖果

> 原文：<https://hackaday.com/2011/12/15/twitter-enabled-candy-machine-dispenses-treats-on-command/>

![twitter-enabled-candy-dispenser](img/9499da18ce26f92d583f8824840d2ff7.png "twitter-enabled-candy-dispenser")

[Michael Nilsson]和[Markus Olsson]正在考虑如何激励他们开发团队的成员，这时他们想到了一个主意:当有人赢得糖果时，糖果机会自动分发糖果。

他们拿起一台糖果机，一个连续旋转伺服系统和一个控制器，然后忙于自动售货机。正如你在[迈克尔的]文章中所看到的，操作背后的机制实际上非常简单。他们拆卸了机器，从手动曲柄上取下齿轮，把它连接到伺服机构上。一旦伺服安装到位，他们安装伺服控制器，并将其连接到一个备用笔记本电脑。

繁重的工作由一个 Ruby 脚本来完成，它使用 Twitter API 来收集任何提到@_macke_ 或@sidpiraya 的内容。收到的信息会被检查“给”和“糖果”这两个词，从而触发机器分发一些糖果。

如果你认为他们的努力值得一点认可，请随时通过推文“give @_macke_candy”或“give @Sidpiraya candy”给他们发送一些糖果。请记住要考虑周到——没有人喜欢垃圾邮件，甚至糖果机也不喜欢！

如果你有兴趣看这部机器的运行，一定要去看看 giveawaycandy.com 的糖果自动售货机的直播。