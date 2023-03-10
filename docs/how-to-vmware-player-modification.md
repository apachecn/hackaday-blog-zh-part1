# 操作方法:VMware Player 修改

> 原文：<https://hackaday.com/2005/10/24/how-to-vmware-player-modification/>

上周，免费的 VMware 播放器发布了。它允许您运行虚拟机，但不能创建它们。[Faileas]贡献了今天的如何创建您自己的虚拟机。

实施黑客攻击所需的程序:

1.  VMware 播放器的副本

2.  [Browser appliance](http://www.vmware.com/vmtn/vm/) 或另一个虚拟机(Browser appliance 是最小的一个，因此我正在使用它)

3.  记事本或其他文本编辑器

4.  FreeDOS 的 ISO 镜像或 CD/软盘(我用的是 [ripcord 发行版](ftp://ftp.ibiblio.org/pub/micro/pc-stuff/freedos/files/distributions/ripcord/current-iso/))或 [MSDOS 7.1](http://www.cn-dos.net/msdos71/) 也可以，但我还没试过。

5.  替换操作系统(必须支持 SCSI 硬盘)

一旦您下载了 browser appliance 或您打算使用的任何映像，第一步是打开并编辑 browser-appliance.vmx 文件。虽然任何文本编辑器都应该这样做，但我使用了记事本。

尽管这些是我的建议，我还是建议根据需要更改设置。将 memsize 的值从 256 更改为 64。对于大多数操作系统来说，这已经足够了，您可以在以后根据需要进行更改。

**第 1 部分:使用 ISO**
我正在使用的映像已经被设置为使用我系统的物理 CD-Rom 驱动器。当你想从一个下载的 ISO 安装时，这不是很理想。虽然可以选择使用 daemontools 或类似的 CD 安装程序，但更好的方法是使用 VMware player 自己读取 iso 的能力。

此时，我建议保存 browser-appliance.vmx 文件并制作副本，因为以后可能需要使用物理 CD-Rom 驱动器。

为此，请替换:
`ide1:0.fileName = "auto detect"
ide1:0.deviceType = "cdrom-raw"`

带:
`ide1:0.fileName = "C:targetcd.iso"
ide1:0.deviceType = "cdrom-image"`

其中 C:targetcd.iso 是您打算使用的磁盘的位置。完成后，保存编辑好的 vmx 文件并运行它。

**第二部分:删除当前操作系统**

现在，在启动屏幕![start screen](img/c15720408fe68750cc81cce4b13c78c0.png)
按下 escape，在下一个屏幕选择从光驱启动。如果一切顺利，迎接你的应该是
![boot](img/b9316fdaf37e15ebe266a30d95ed2797.png)
你应该选择从 CDrom 启动的地方。从那里![menu](img/fd10c91c3f5dcd8e7f547620a3504087.png)
选择引导到第二个选项“FreeDOS ** FAT32”。在下一个屏幕![toreto](img/b835f6a49bcf9d0482b24e1532b20ec3.png)
选择第一个选项，选择“使用 el toreto cd rom 驱动程序引导”(默认)![driver](img/5e2e4552decf675ff5848f535f24c42d.png)
，然后选择第二个选项，从 cd 命令提示符运行 FreeDOS。

现在是有趣的部分