# 希望 2008:冷启动攻击工具发布

> 原文：<https://hackaday.com/2008/07/18/hope-2008-cold-boot-attack-tools-released/>

来自普林斯顿的团队[在](http://citp.princeton.edu/memory/code/)[最后的希望](http://www.mahalo.com/The_Last_HOPE_Conference)发布了他们的冷启动攻击工具。今年早些时候，他们展示了如何从关机的机器的内存中恢复密钥。现在他们已经提供了必要的工具来获取和使用你自己的内存转储。bios_memimage 工具是用 C 编写的，使用 PXE 来启动机器和复制内存。该软件包还有一个磁盘引导转储器，上面有如何在 iPod 上运行它的说明。还有 efi_memimage，它实现了 efi 中的 BSD TCP/IP 堆栈，但这可能会有问题。aeskeyfind 可以从内存转储中恢复 128 位和 256 位 AES 密钥，rsakeyfind 可以为 RSA 恢复同样的密钥。他们还提供了 aesfix 来纠正高达 15%的键。在测试中，他们只看到 0.1%的内存转储错误，如果他们先冷却芯片，则只有 0.01%。

我们今天看到了另一个有趣的工具: [coreinfo](http://www.coreboot.org/Coreinfo) 是一个定制 BIOS coreboot 的库。使用它，你可以直接检查内存，没有任何损害。

[Jacob Appelbaum]演讲结束时的问答环节包括对可能对策的讨论。我们确信，在 RAM 设计发生根本性变化之前，这个问题不会得到解决。我们听到的一个有趣的建议是制造一个“公羊避孕套”。RAM 插入的将是一个 riser 卡。当入侵系统触发时，它会清空内存。这是一个有趣的想法；有人想建吗？

*   [永久链接](http://citp.princeton.edu/memory/code/)