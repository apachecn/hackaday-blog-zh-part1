# P-FET 反向电压保护

> 原文：<https://hackaday.com/2011/12/06/reverse-voltage-protection-with-a-p-fet/>

[Afroman 的]最新视频向您展示如何[在最小功耗的情况下添加反向电压保护](http://www.youtube.com/watch?v=IrB-FPcv1Dc)。在某些时候，你的一个电子产品会变得非常有用。你要确保电池插错了，或者 PSU 的极性错误不会损坏硬件。加入二极管进行保护很容易，但正如[阿弗曼]指出的那样，当电路正常工作时，这会以热量的形式浪费能量。他的解决方案是增加一个 P 沟道 MOSFET，只有当电源电压的极性正确时，它才允许功率流动。

上面的原理图显示了电路高端的 P-FET。栅极接地，当连接电池时，允许电流流过 DS 结。该设计还使用箝位二极管将栅极电压保持在安全范围内。但也有不需要二极管或电阻的 P-fet。这种方法比简单的二极管消耗的能量少 10 倍。

我们在休息后嵌入了视频，视频中[一名妇女]分享了他选择组件背后的数学和推理。

[https://www.youtube.com/embed/IrB-FPcv1Dc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/IrB-FPcv1Dc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)