# 4D 系统微驱动器

> 原文：<https://hackaday.com/2009/07/21/4d-systems-micro-drive/>

![p1193335689](img/041d0300bad9da12f2ad46f63e5b9b92.png "p1193335689")

[4D 系统公司的 micro drive](http://www.4dsystems.com.au/prod.php?id=22) 提供对 microSD 卡的原始和 FAT 级访问。该模块包含一个专用的主机控制器，可以将原本令人生畏的卡规格转换为一组简单的串行命令。具有 3.6-5.5 的宽电源范围和 0.1 英寸的引线间距，这应该是小菜一碟。该设备尚不支持 FAT32。根据 [GOLDELOX-DOS 命令集](http://www.4dsystems.com.au/downloads/micro-DRIVE/uDRIVE-uSD-G1/Docs/Pdf/GOLDELOX-DOS-COMMANDS-SIS.pdf)第 9 页，“FAT32 目前不被支持，如果你挂载一个 FAT32 格式的磁盘，你将根本无法访问它，FAT 和 RAW 命令都将失败”。目前，该设备似乎仅限于 2GB FAT16 分区。在实现 SPI 和半字节模式 SD 卡协议后，这确实看起来像作弊。

Electronics-Lab.Com 感谢莫兹瓦尔德