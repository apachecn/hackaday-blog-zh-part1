# 跨平台多点触控

> 原文：<https://hackaday.com/2008/11/28/tbeta-cross-platform-multitouch/>

[https://player.vimeo.com/video/2034557](https://player.vimeo.com/video/2034557)

tbeta 是由 NUI 集团开发的新工具。tbeta 充当图像处理层，接收图像数据并输出多点触摸应用的跟踪数据。无论是 [FTIR](http://wiki.nuigroup.com/FTIR "Frustrated Total Internal Reflection (FTIR) - NUI Group") 还是 [DI](http://wiki.nuigroup.com/Diffused_Illumination "Diffused Illumination (DI) - NUI Group") ，scratch 构建的多点触摸系统都会生成红外视频流，需要对其进行处理才能找到指尖。tbeta 可以获取该视频流或任意视频流，并通过一系列过滤器来生成触摸数据。该数据作为 OSC [TUIO](http://mtg.upf.edu/reactable/?tuio "reactable tuio") 发送，这是触摸事件的标准协议。除了摄像头和输入切换器之外，tbeta 还有助于系统校准。我在 Windows、OSX 和 Linux 上工作。请看一下[入门指南](http://wiki.nuigroup.com/Tbeta_-_Getting_Started "Getting Started with tbeta - NUI Group")以更好地了解它是如何工作的。

[通过 [CDM](http://createdigitalmotion.com/2008/11/25/tbeta-open-source-computer-vision-multi-touch-sensing-follows-your-fingers/ "Open-Source Computer Vision, Multi-touch Sensing Follows Your Fingers")