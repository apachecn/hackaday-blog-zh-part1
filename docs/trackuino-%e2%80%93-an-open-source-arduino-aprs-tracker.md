# track uino——开源的 Arduino APRS 追踪器

> 原文：<https://hackaday.com/2011/04/20/trackuino-%e2%80%93-an-open-source-arduino-aprs-tracker/>

[![trackuino board](img/20b8ff6f9a0183076f816c718344049d.png "trackuino_board (Custom)")](http://hackaday.com/2011/04/20/trackuino-%e2%80%93-an-open-source-arduino-aprs-tracker/trackuino_board-custom/)

Trackuino 是由[Javier Martin]设计的一个新的开源(GPLv2 许可)Arduino APRS 追踪器。如果你不熟悉:APRS(自动数据包报告系统)是一种业余无线电方法，用于将小数据包的位置跟踪数据中继到在线数据库，以便于访问和映射。在这种情况下，GPS 遥测数据用于通过 [aprs.fi](http://aprs.fi) 近乎实时地跟踪纬度、经度、高度、航向、速度和时间测量值。

虽然这让我们想起了我们之前讨论过的[where VR](http://hackaday.com/2009/05/08/whereavr-aprs-tracker/)，但 Trackuino 包括一个车载无线电，因此不需要外部手持单元。由于 Trackuino 主要是为高空气球跟踪而设计的，因此还包括了一些有用的相关功能:双温度传感器、对湿度传感器的支持以及远程“下调”触发器，使这真正成为一个完整的包。

最初有人担心所用的 300 兆瓦无线电功率不足以从高峰高度到达地面接收器。然而，这显然不是问题，因为在[首航](http://crocketteng.com/blog/)期间，信号是从近 600 公里外听到的。如果这听起来还不够大，还支持 500mW 的无线电。

请务必查看[【Javier】的博客](http://trackuino.blogspot.com/)，获取一些令人惊叹的高空照片和让您自己的 Trackuino 快速启动并运行所需的一切！

谢谢[布拉德]！