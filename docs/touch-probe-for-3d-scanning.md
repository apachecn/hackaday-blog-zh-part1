# 用于 3D 扫描的触摸探头

> 原文：<https://hackaday.com/2006/04/19/touch-probe-for-3d-scanning/>

![touch probe](img/0efa4b2a5872703f33d8bc122244d3c1.png)

格雷厄姆称这个[触摸探头](http://www.indoor.flyer.co.uk/probe.htm)为他的第一个有用的铣削项目。他已经建立了数控轧机，一旦他在轧机上建立了这个探针，他基本上有一个三维扫描仪。中心轮毂由三根围绕其轴线均匀分布的轴支撑。这些轴分别靠在一对滚珠轴承上，形成一个完整的回路。如果探针碰到任何东西，其中一个轴就会抬起，切断电路。 [TurboCNC](http://www.dakeng.com/turbo.html) 有一个内置的程序，可以用触摸探头进行扫描。该程序生成一个点文件，Graham 将该文件拉入 [Rhino](http://www.rhino3d.com/) 进行建模。他的示例应用程序是克隆一个已经停产的飞机模型。TurboCNC 程序不是很快，因为探头总是返回到相同的高度，所以他编写了一个更快的算法。agiecco 的[乐高 3D 扫描仪](http://mindstorms.lego.com/eng/inventions/invention.asp?id=%7BAAFA7565-8EEF-CED9-1284-6A1A7A689712%7D&SlotN=1&galleryid=347)也采用了这种基于触摸的扫描方式。

*   [永久链接](http://www.indoor.flyer.co.uk/probe.htm)