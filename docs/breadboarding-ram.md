# 试验板 RAM

> 原文：<https://hackaday.com/2010/11/14/breadboarding-ram/>

![](img/4f536957b549a85b181ea41bf1e971f3.png "BJT memory")

如果你想深入了解一下内存硬件是如何实现的，这里有一个很好的例子，说明如何用以太 [BJT](http://www.instructables.com/id/DIY-RAM-Memory-Register-Style/step3/The-Circuit/) 或 [CMOS](http://www.instructables.com/id/DIY-CMOS-RAM-Memory/) 晶体管实现一些锁存电路。BJT 需要偏置电阻，与 CMOS 相比，这增加了复杂性和功耗。如果功耗不是问题，你当然可以做一些真正快速的逻辑[。](http://en.wikipedia.org/wiki/Emitter-coupled_logic)

大多数现代的片上 RAM 都是使用 [SRAM](http://en.wikipedia.org/wiki/Static_random_access_memory) 制成的，因为它只需要 6 个晶体管(而不是 8 个)就能实现，而且速度非常快。谈到密度 [DRAM](http://en.wikipedia.org/wiki/Dynamic_random_access_memory) 可以通过使用单个晶体管和电容器获得一位存储(将电容器放在晶体管下面可以节省更多空间)。尽管如此，在处理数字电路时，锁存器和触发器仍然是一个非常有用的(和常见的)工具。