# 如何:有竞争力地折叠@Home

> 原文：<https://hackaday.com/2005/09/13/how-to-foldinghome-competitively/>

![folding](img/23b2d7e6192a6bfc87d8ae5bad3f3932.png)

**更新:**要解决你的 F@H 设置问题，去非官方的[团队黑客日论坛](http://teamhackaday.com)。

*在上周宣布[一天黑一次的折叠团队](http://vspx27.stanford.edu/cgi-bin/main.py?qtype=teampage&teamnum=44851)之后，它已经成为[增长最快的团队](http://folding.extremeoverclocking.com/team_list.php?s=&srt=9%22)之一。[BillytheImpaler]整理这份伟大的指南，不仅可以帮助您开始折叠，还可以让您的机器发挥出最佳的折叠性能。请继续阅读并加入我们的团队，这样我们就可以进入前 1000 名！*

[来自维基百科](http://en.wikipedia.org/wiki/Folding_at_Home)

> Folding@home 是一个分布式计算项目，旨在执行蛋白质折叠的计算密集型模拟。该项目的目标是加深对蛋白质折叠、错误折叠、聚集和相关疾病的理解。这些疾病包括疯牛病、克罗伊茨费尔特-雅各布病、阿尔茨海默病、帕金森病等。
> 
> Folding@home 的处理不依赖强大的超级计算机；相反，Folding@home 项目的主要贡献者是成千上万安装了小型客户端程序的个人电脑用户。客户端在后台运行，并在不忙时使用 CPU。在大多数现代个人电脑中，中央处理器很少总是被充分利用；Folding@home 客户端利用了这种未使用的处理能力。

Folding@home 客户端定期连接到服务器以检索“工作单元”，这些“工作单元”是根据
执行计算的数据包。然后，每个完成的工作单元被发送回服务器。

从硬件黑客的角度来看，这是一个个人和团队竞相在最少的时间内完成最多的工作的项目。本指南旨在帮助新文件夹适应程序
以及如何操作它，也帮助有经验的文件夹调整他们的安装，以充分发挥
的性能。

## 入门指南

去斯坦福的网站[下载合适的客户端](http://folding.stanford.edu/download.html)。
任何拥有运行 Windows 9x、NT、XP、Mac OSX 和 Linux 的个人电脑的人都会在那里找到客户。BSD 用户
一般运行 Linux 客户端。

**挑选客户**

有几种不同的客户端可用；文本控制台，图形用户界面和屏幕保护程序。

就速度而言，文本控制台> GUI >屏保。同样，客户的速度也不同；Windows > Linux > OSX 这是因为每个平台都有编译器。Linux 用户可以通过在 WINE 中运行 Windows 控制台来获得
速度。

如果你追求性能，不要运行屏保版本。仅仅是绘制漂亮的蛋白质图像就浪费了大约 15%的 CPU 能量。众所周知，GUI 版本会干扰一些游戏，所以我强烈推荐
控制台版本，尤其是对那些每天都在黑电脑的普通观众。

本指南将重点介绍 windows 的控制台版本，因为它具有最佳性能，是最受欢迎的选择。

**设置**

通过使用 windows 打开控制台或通过命令行执行来运行控制台。

*   用户名**【输入用户名】**选择一个没有其他 H-A-D 文件夹选择的用户名
*   团队编号**【44851】**
*   在机器启动时自动启动，将其作为服务安装**【是】**
*   取/发前询问**【否】**
*   使用 internet explorer 设置是/否**如果有代理，则为是，否则为否**
*   使用代理是/否**同上**
*   允许接收工作分配并返回大小超过 5MB 的工作结果(这种工作单元可能有
    大的内存需求)是/否(如果您将机器用于 F@H 之外的事情，并且 RAM 少于 256 MB
    **否**，否则**是**，因为这些单元得到更好的分数)
*   更改高级选项**【是】**
*   核心优先级**【空闲】**
*   CPU 使用率**【100】**
*   禁用高度优化的汇编代码**【否】**
*   使用电池电源时暂停(适用于笔记本电脑)是/否
*   检查点之间的间隔，以分钟为单位(3-30) **【我选择 15】**
*   要求无截止日期的工作单位**【否】**
*   忽略任何截止日期信息(主要在系统时钟出错时有用)**【否】**
*   机器 ID(1-8)**【1】**

程序现在将下载一个 WU 并开始计算。

按 Ctrl-C 暂时退出。

打开注册表编辑导航 HKEY _ 本地 _ 机器系统当前控制设置服务 sFAH@C…

您将在图像路径中设置关键点。之后。请键入一个空格。并输入以下键:

**对于所有 AMD 64 和英特尔 P4，至强(非奔腾移动)**

-local 将 F@H 文件保存到与控制台相同的目录中

-verbosity 9 向日志文件输出客户端允许的最多数据

-forceasm 强制 F@H 使用 SSE 和 3DNow 程序集优化

-advmethods 客户只要求最新的 WUs*** * * P4S 上的 VITAL * * ***P4s 上的 this，结合 Big
WUs=yes 将为您获得 QMD 工作单位。前 1-2%使用 300 MB RAM，之后使用 200 MB。因为
他们使用了这么多的系统内存，他们得到了*奖励点*这些单位是最好的，因为他们是如此之快
和如此高的分数。如果你有 P4，你可以得到这些，所以我建议你这样做。

***QMD 注意*** 由于 _all_ AMD athlons 不支持 SSE2 和 SSE3，因此没有人会收到 QMD 工作单位。
qmd 是英特尔独有的聚会，相信我，他们是一个聚会。未来，F@H 将包含一个类似 CPU-Z 的功能
，它专门识别硬件，以便更好地使用参与者的计算机。预计这个版本将于 2006 年初在
问世。

**对于奔腾手机**

(哪些是 F@H 的出色表演者)

-本地

-力 asm

详细程度 9

最近，通过不设置-advmethods，我得到了更好的 WUs(更多的 600 个指针)，我不知道为什么，看起来这就是斯坦福一直在做的事情。

重新启动机器以启动服务。

**双核、P4 超线程和双处理器机器的设置**

除了这些东西之外，设置完全相同。

将控制台的另一个副本放在一个*不同*的目录中。否则它们会互相干扰。

将 2 号的机器 ID 设为 2，3 号设为 3，依此类推。最多 4 个。(对于那些使用四路 P4EEs 的人，很抱歉，客户端
不支持您的 16 个逻辑单元。)

GUI 客户端不可能同时使用两个内核/虚拟内核，所以这是使用命令
行版本的另一个原因。

奔腾 4s 中的超线程是非常有价值的。运行 2 个 100%的客户端会比 1 个 100%的客户端运行得慢，但是
它会在另一个客户端完成 1.5 个单位的时间内完成 2 个单位。因此，从长远来看，它更快。在我的 P4 上，我用 512 MB 内存同时折叠了两个 qmd，它非常稳定。你可能不会这么幸运。如果您不希望
接收某个进程的 qmd，请移除-advmethods 标志。

单处理器 P4 机器的好处在于，你可以在一个线程上运行 F@H，在 HT 给你的另外 15%的时间上运行操作系统 web 浏览器
等等。这意味着你不会因为使用机器而减慢你的进度。

## 运行 F@H

禁用任何屏幕保护程序，因为它们会占用你宝贵的空闲处理周期。我把我的设置成 5 分钟后空白，10 分钟后关闭(为了省电)。如果可以的话，24/7 都不要动你的机器。关机的电脑什么都不会计算。如果你有说服力的话，招募其他人加入你的用户名下。

当你完成一个武后，你将出现在[统计
页面](http://vspx27.stanford.edu/cgi-bin/main.py?qtype=teampage&teamnum=44851)上。数据库服务器大约每 3 个小时更新一次，所以你可能要等几个
小时才能看到你单位的证据，但是他们会出现的。你可以用
[FAHMON](http://fahmon.silent-blade.org/) 或
[emii](http://home.comcast.net/%7Ewxdude1/emsite/download.html)来监控你的进度。我更喜欢 FAHMON，因为它运行时使用的内存少得多，启动速度也更快。EMIII 功能更强大，以蛋白质可视化为特色，并且能够通过网络监控多个客户端。用哪个都行。

要禁用游戏、编译视频编码或其他任何您想要的服务，请运行 services.msc，
向下滚动到 FAH 进程，单击每个进程并选择“停止服务”再次重复此操作以重新启动它。我在运行 F@H 的机器上玩游戏，但如果你打算做任何真正踢你电脑屁股的事情(毁灭战士 3，
半衰期，诸如此类的事情)，请随时停止。

**超频**

官方说法是，斯坦福对超频嗤之以鼻，因为它会导致模拟不稳定。然而，这是一个硬件黑客的网站，所以我将讨论它。如果您的机器严重超载，并且您在
团队统计页面上看到奇怪的统计报告，即返回了 5 个工作单位但获得了 5 分，您可能会看到工作提前结束(母羊)。
这些是模拟达到无法继续的地步。这通常是由不稳定的 OC，
引起的，尽管并不总是如此。如果是这种情况，你应该把你的 OC 调小一点，以增加系统的稳定性。如果一个 OC-d 钻机
太不稳定而无法执行代码，那么它对任何人都没有用。我有一台 P4 诺斯伍德 2.4GH，我运行在 3.1GHZ
非常稳定的股票惠普散热器，所以它当然有可能 OC 和折叠，只是不要做得太多。

**Borging**

以星际迷航同化竞赛命名，Borging 指在某人的电脑上安装 F@H 或任何 DC 程序，通常在他们不知情的情况下。这是 EULA 明令禁止的，但人们还是这么做了。我有几本书，所以我不会告诉你不要去做。小心点，有人因为抢劫 T4 而被 T2 T3 解雇了。有一个程序
是由一个每日黑客团队成员编写的，它检查计算机的硬件设置，并根据 ram 的多少、CPU 的速度、CPU 的数量等做出决定。哪种方式安装 F@H 可获得最佳、最小的侵入性性能。我希望
在这篇文章中有一个测试版，但是它还没有完全准备好，所以你必须等待
让你的 b0rg 上线。

## 结论

玩得开心。这就是大多数人跑 F@H 的原因。这与其说是科学，不如说是竞争和友情。折叠是一种瘾；人类已知的为数不多的健康嗜好之一。我们团队 Hack-A-Day 是这个星球上发展最快的团队之一，我们希望在下个月内进入全球前 1000 名。
所以加入吧，关注你的数据，玩得开心。开始咀嚼吧，伙计们。