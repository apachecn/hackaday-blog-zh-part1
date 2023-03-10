# Kinect 和 TISCH 结合用于多点触控

> 原文：<https://hackaday.com/2010/11/13/kinect-and-tisch-combined-for-multitouch/>

![](img/cb2810a2964278f90daa33fd1775ed2a.png "kinect-multitouch")

[Florian]发送了一个链接，链接到[他使用 Kinect 创建多点触摸显示屏的概念验证](http://www.youtube.com/watch?v=ho6Yhz21BJI)。他是[libTISCH 多点触控套件](http://hackaday.com/2009/10/29/libtisch-1-0-released/)的幕后推手，这是他用来让这个套件与[最近发布的 Kinect 驱动程序](http://hackaday.com/2010/11/11/open-source-kinect-contest-has-been-won/)一起工作的。他在一台 Ubuntu 机器上做了这个，虽然这不是一个交钥匙的解决方案，但他还是很友好地分享了一些自己完成它的粗略指导。休息后请加入我们，观看他的指导和一些嵌入的视频。

当我们问他是否能向我们介绍如何复制他的作品时,[Florian]是这样回答的:

> 我会试试看，但这真的很难:-)你需要
> 
> –Ubuntu 10.10
> –一台 Kinect(惊喜:-)
> 
> –来自[https://github.com/OpenKinect/openkinect](https://github.com/OpenKinect/openkinect)
> 的 OpenKinect 驱动程序–转到目录 open Kinect/c/
> –编辑 lib/CMakeLists.txt，使其显示“add_library (freenect SHARED ..”
> –运行“cmake”
> –运行“制作”
> 
> –TISCH 库，1.1 分支
> –SVN co[https://TISCH . SVN . SourceForge . net/SVN root/TISCH/libtisch-1.1](https://tisch.svn.sourceforge.net/svnroot/tisch/libtisch-1.1)
> –编译类似:
> CFLAGS =-I/foobar/open Kinect/c/include \
> LD flags = "-L/foobar/open Kinect/c/lib-lfreenect "
> make install
> –转到 libtisch-1.1/build../lib/"
> –运行"。/touchd -Vf "
> 
> –如果第一次尝试不成功，编辑~/. tisch . touch d
> –在具有分辨率的行(第 5 行)，更改为类似于
> "640 480 30 5 127 8 255 0 "的内容
> 
> –使用~/.tisch.touchd 设置文件(我知道它非常
> 可怕，格式在这里有所记载:
> [http://sourceforge.net/apps/mediawiki/tisch/index.php?title=Touchd_config](http://sourceforge.net/apps/mediawiki/tisch/index.php?title=Touchd_config) )。
> 
> 嘿，现在我读了，我很惊讶它竟然真的有效:-)
> 
> 弗洛里安

您的结果可能会有所不同，所以请在下面的评论中留下您的任何提示。

[https://www.youtube.com/embed/ho6Yhz21BJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ho6Yhz21BJI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)