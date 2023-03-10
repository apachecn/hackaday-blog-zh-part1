# 将 PDP-10 放在 FPGA 上

> 原文：<https://hackaday.com/2011/07/29/putting-a-pdp-10-on-an-fpga/>

[![](img/e222a2b408403ddd81ec72ba6cd53339.png "PDP")](http://hackaday.com/wp-content/uploads/2011/07/pdp1.jpg)

在过去的两年半时间里，[dgcx]一直致力于在 FPGA 上重新实现 PDP-10/x。这让我们很惊讶，因为我们现在才听说这个项目*。*

 *在设计了三个版本之后，[dgcx]最终以 PDP-10 的单 FPGA 实现和令人惊叹的[PDF 文章](http://homepage.mac.com/dgcx/pdp10x/pdp10x.pdf)而告终。虽然 [PDP-10 仿真器](http://www.aracnet.com/~healyzh/pdp10emu.html)确实存在，但这个项目不是仿真——该系统实际上具有原始的 36 位字长，在五个 4096 千位 SRAM 芯片上实现。这是一个全功能的复制品，甚至用一个小型以太网控制器实现了[混沌网](http://en.wikipedia.org/wiki/Chaosnet)。

就像 FPGA 上的微型 Cray-1 一样，剩下唯一要做的就是将 PDP-10 克隆体放入一个令人敬畏的盒子中，就像 T2 的 PDP-1 复制品一样。我们想象[dgcx]可以相当容易地得到真正 PDP-10 的[数字模型](http://hackaday.com/wp-content/uploads/2011/07/tf2.png)。

对于非常旧的计算机，很难找到在这些机器上运行的软件。这也是小克雷的制造者遇到的问题。如果任何 Hack A Day 的读者知道[dgcx]在哪里可以找到一些旧的 DEC 软件，一定要在评论中发表一些东西。否则，他可能刚刚开始移植 Unix 的第一版。*