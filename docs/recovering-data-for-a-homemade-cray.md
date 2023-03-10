# 为自制的 Cray 恢复数据

> 原文：<https://hackaday.com/2011/09/08/recovering-data-for-a-homemade-cray/>

![](img/bc2f795346a737e48d59ff6f2aa15b79.png "cray")

在我们的傲慢中，当我们能够从我们的旧 SCSI 驱动器中取出数据时，我们会拍拍自己的背。[克里斯·芬顿]试图为自制软件 Cray-1 获得一个操作系统，这让我们理所当然地感到羞愧。

去年，我们看到[Chris]' [围绕 FPGA 构建的全功能 1/10 规模的 Cray-1 超级计算机](http://hackaday.com/2010/09/29/tiny-cray-1-courtesy-of-an-fpga/)。虽然复制几乎是准确的周期，[克里斯]还没有机会测试他的系统，因为缺乏可用的克雷软件。一名前 Cray 雇员听说了他的困境，将一个 80 兆字节的 CDC 9877 磁盘包借给了微软，希望得到一些系统软件。

[克里斯]获得了一个巨大的 100 磅[磁盘驱动器](http://chrisfenton.com/wp-content/uploads/2011/09/cdc9762.jpg)来读取磁盘组，但是在存储了 30 年之后，出现了许多电气问题。由于以数字方式读取硬盘被证明是徒劳无益的，所以[Chris]想到了直接从读取头获取模拟数据的想法。这给他留下了磁盘组的磁性图像，准备进行一些数据分析。

在[磁盘映像](http://www.archive.org/details/cray-disk-project)被放到互联网上后，非常有才华的【Yngve AAdlandsvik】弄清楚了数据、标题和纠错格式，并给【Chris】发送了一个 Python 脚本来从模拟映像中提取比特。虽然没有人十分确定 Cray 员工提供的磁盘包中有什么，但[Chris]非常接近于让 Cray-1 OS 起死回生。还有一个伟大的[研究报告](http://www.archive.org/stream/2011-cdc-disk-archaeology-fenton/summer_2011_final_small#page/n0/mode/1up)【克里斯】写道，作为进入 CDC 磁盘驱动器的忏悔。《黑客一天》的读者想看看这些数据，并尽可能帮帮克里斯吗？