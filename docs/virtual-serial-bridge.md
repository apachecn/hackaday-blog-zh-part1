# 虚拟串行桥

> 原文：<https://hackaday.com/2011/03/24/virtual-serial-bridge/>

![](img/badbe1f6200270266112b49629df1c07.png "Screen_shot_2011-03-22_at_8.20.12_PM")

当您运行模拟器或虚拟机时，有时将一个串行端口从客户机连接到主机可能会很方便。[Aurimas]有这个问题，也有一个有趣的修复方法，使用 2 个 USB <>串行适配器，但正如你可以想象的那样，这不是一个理想的解决方案，进入[虚拟串行桥](http://blog.gcds.lt/2011/03/22/socat-virtual-serial-bridge/)。

深入了解 Vmware 后发现，他所需要的支持是有的，但并未真正使用。在来宾操作系统 vmx 文件中添加几行代码，并配置 socat 多用途中继包。虽然这些说明围绕着 Mac 平台作为主机，windows 作为客户 socat 和 Vmware，但您可能会将它与任何使用串行端口和*x 或 Windows 主机的软件混合使用。