# 用 CPU 缓存防止冷启动？号码

> 原文：<https://hackaday.com/2009/01/18/use-the-cpu-cache-to-prevent-cold-boot-no/>

![coldboot](img/48542fc7aab404c6a6102b3061c21ecb.png "coldboot")

[冷冻缓存](http://frozencache.blogspot.com/ "Frozen Cache")是一个博客，致力于一种新颖的方法来防止[冷启动攻击](http://citp.princeton.edu/memory/)。去年，冷启动团队[展示了](http://hackaday.com/2008/05/13/cold-boot-encryption-attack-video/ "Cold boot encryption attack video  - Hack a Day"),他们可以通过将一台机器放入另一个系统(或者通过快速重启同一台机器)来从它的 RAM 中提取加密密钥。冻结缓存旨在通过将加密密钥存储在 CPU 的缓存中来防止这种情况。它把 RAM 中的密钥复制到 CPU 的寄存器中，然后在 RAM 中置零。然后，它冻结缓存并尝试将密钥写回 RAM。键被推入缓存，但不写回 RAM。

这方面的第一个主要问题是性能下降。当你冻结缓存时，你最终会使处理器瘫痪，作者建议你只在屏幕被锁定时才这样做。我们询问了冷启动团队成员[ [Jacob Appelbaum](http://appelbaum.net/) ]对这种方法的看法。他指出，当前的冷启动攻击从完整的密钥表中重建密钥，根据冻结缓存博客，该密钥表仍保留在 RAM 中。它们不是获取特定的关键位，而是从内存中的所有冗余信息中重新创建它。充其量，冻结缓存试图建立一个“贫民窟加密协处理器”。

我们袖手旁观对冷启动攻击的最初反应是:在这个问题解决之前，需要对 RAM 进行一次根本性的重新设计。

[通过[斜线圆点](http://it.slashdot.org/article.pl?sid=09%2F01%2F18%2F2110235 "Slashdot | Solution Against Cold Boot Attack In the Making")