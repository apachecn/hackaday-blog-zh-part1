# 用 FPGA 模拟化学反应

> 原文：<https://hackaday.com/2011/07/19/modelling-chemical-reactions-using-an-fpga/>

![](img/82db624ddf1e44247cdb6c1912781b80.png "fpga-chemistry-modelling")

[Bruce Land]是康奈尔大学的一名教授，他正在寻找一种快速解决化学动力学系统的方法。他用过 MATLAB，但渴望一种更快的方法。他的升级通过使用 FPGA 作为并行随机解算器实现了 100 倍的速度提升[。](http://people.ece.cornell.edu/land/courses/ece5760/Chemical_Simulation/index.html)

它的工作原理是利用 Altera DE2 板产生 100 个伪随机 16 位数字。这个过程在 50 MHz 下每个周期进行一次，所以我们讨论的是许多随机数。它们通过求解器算法运行，并用于计算每个反应周期。在运行 MATLAB 版本的 3.8 GHz P4 进程中，其中一个周期大约需要 1000 秒，因此速度的提高可以立即感觉到。有这个新工具真是太好了。这确实让我们想知道用我们见过的破解密码或挖掘比特币的 GPU 处理能做些什么。就像 FPGAs 一样，GPU 非常适合运行大量并行操作。