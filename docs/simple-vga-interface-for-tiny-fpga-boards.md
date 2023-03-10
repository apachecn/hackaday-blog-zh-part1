# 小型 FPGA 板的简单 VGA 接口

> 原文：<https://hackaday.com/2011/06/02/simple-vga-interface-for-tiny-fpga-boards/>

![fpga_vga_adapter](img/f8ad5de857c8f4c30a469690f7fab32f.png "fpga_vga_adapter")

[devb]已经使用 XESS FPGA 板很多年了，从他记事起，它们就有内置的 VGA 接口。他最新收购的 XuLA FPGA 板除了 USB 连接器之外，没有任何外部部件或端口。他需要从板获得视频输出，所以他决定自己构建一个 VGA 接口。

他制作了一个 512 色 VGA 接口板的原型，运行良好，但他认为它太笨重了，无法用于每个项目。为了简化生活，他设计了一个小型 PCB，集成了一个 VGA 连接器和从 FPGA 获取信号所需的所有电阻。他的电路板直接插入试验板，所以只需要几根电线就可以将 FPGA 连接到显示器上。

正如你在他的网站上看到的，适配器工作得很好，允许 FPGA 毫不费力地输出清晰的 800×600 图像。[devb]还在他的网站上以 Eagle 格式发布了他所有的设计文件，供任何有兴趣复制他作品的人使用。