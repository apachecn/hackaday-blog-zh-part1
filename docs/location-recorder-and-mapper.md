# 位置记录器和测绘仪

> 原文：<https://hackaday.com/2011/02/03/location-recorder-and-mapper/>

![](img/1c990b954dd90c380adf270211a02d05.png "gps-location-tracking-mapping")

[耶鲁安的]学生项目是一个使用[GPS 追踪在谷歌地图](http://gpstracer.blogspot.com/2011/02/gps-tracer-for-school-stenden.html)上创建旅行数据的模块。这不是一个真正的间谍设备，因为数据不会被传输，但在骑自行车和徒步旅行冒险中使用会很有趣。PIC 18F2550 从 GPS 接收器读取位置和高度数据，以及从加速度计读取数据。该信息可以显示在相连的触摸屏上，也可以保存在一对 EEPROMs 中。当你旅行回来时，通过串行连接从设备中提取的数据由[耶鲁安的] C#应用程序处理，并用于在谷歌地图上覆盖路线。他有一个源代码包可供下载，但如果您只需要原理图，我们已经帮您省了麻烦。休息后附上。

[![](img/cc72cdb36ec06514bc2886ef1ce5b047.png "gps-tracer-schematic")](http://hackaday.com/wp-content/uploads/2011/02/gps-tracer-schematic.png)