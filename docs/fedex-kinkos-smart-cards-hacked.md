# 联邦快递 Kinko 的智能卡被黑

> 原文：<https://hackaday.com/2006/03/02/fedex-kinkos-smart-cards-hacked/>

![fedex](img/c400f9028976d5c08c10eca05d24f3c0.png "fedex")

安全科学公司的研究人员已经成功[破解了联邦快递 Kinko 商店使用的快递支付系统](http://www.mal-aware.org/2006/02/28/fedex-kinkos-smart-cards-hacked/)，该系统由 enTrac 提供。这些卡使用 3 字节安全码进行写保护。您可以使用逻辑分析仪嗅探这些数据，然后使用代码将您想要的任何数据写入卡中，因为它是未加密的。所有卡的安全码都是一样的。联邦快递金考公司声明这篇文章是不准确的，所以兰斯·詹姆斯和斯特罗姆·卡尔森制作了一个他们在商店进行黑客攻击的[视频:他们在售货亭的一张卡上放入 1 美元，然后用它登录到一台计算机，显示 1 美元的余额。他们注销并使用单独的笔记本电脑和读卡器/写卡器将余额改为$50.00 并修改序列号。接下来，他们使用该卡重新登录计算机，并显示 50 美元的余额。他们让一分钟过去了，所以从卡上扣了 0.20 美元。最后，他们注销并使用自助服务亭打印出一张收据，显示他们的余额为 49.80 美元，带有假序列号。此时，攻击者可以将卡拿到服务柜台，要求支付现金余额。](http://www.securescience.net/exploits/ssc_expresspay_vuln.wmv)

[感谢来自[午夜研究室](http://midnightresearch.com/)的西斯]

[修复:我最初说过他们在信息亭买了一张新卡]

[图片: [caribb](http://flickr.com/photos/caribb/2498637518/)

*   [永久链接](http://www.mal-aware.org/2006/02/28/fedex-kinkos-smart-cards-hacked/)