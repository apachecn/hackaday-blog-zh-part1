# 希望 2008:硬件混淆的不可能性

> 原文：<https://hackaday.com/2008/07/18/hope-2008-the-impossibility-of-hardware-obfuscation/>

![](img/934753ec6cc681ad584a9b21b5cce784.png)
[最后的希望](http://www.mahalo.com/The_Last_HOPE_Conference)在纽约开始运行。[Karsten Nohl]首先介绍了硬件混淆的可能性。[卡斯滕]精通这个课题，他曾在一个团队中工作过，这个团队的[破解了 MiFare crypto1 RFID 芯片](http://www.hackaday.com/2008/01/01/24c3-mifare-crypto1-rfid-completely-broken/)。所用的算法是专有的，所以他们的部分研究直接着眼于硬件。正如[bunnie]在他的[Toorcon silicon hacking talk](http://www.hackaday.com/2005/09/20/tc7-day-2-hacking-silicon-secrets-behind-the-epoxy-curtain/)中提到的，即使在考虑安全性之前，硅也很难设计，它必须遵守物理定律(硬件所做的一切都必须物理构建)，并且在制造过程中芯片被逆向工程来验证它。所有这些因素都让黑客非常感兴趣。对于 MiFare 裂缝，他们刮掉了硅层并拍摄下来。使用 Matlab，他们直观地识别各种门，并寻找类似密码的部分。如果你对这些逻辑单元的样子感兴趣，[卡斯滕]已经组装了[硅动物园](http://siliconzoo.org/)。动物园里有标准单元的图片，如反相器、缓冲器、锁存器、触发器等。看看[Chris Tarnovsky]的作品，了解他如何处理智能卡 T10 或[nico]的指南 T12 展示我们在本周早些时候讨论过的标准芯片 T13。