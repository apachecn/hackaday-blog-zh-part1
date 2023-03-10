# 问黑客日:网络安全摄像头

> 原文：<https://hackaday.com/2010/04/10/ask-hackaday-network-security-camera/>

![](img/18316a2df0029e5a64267470ab30f92e.png "While testing out the camera, I accidently pulled the plug on our cable modem. You can imagine how silly I felt after figuring out the problem an hour later.")

今天我们收到了一个问题，

**“如何通过互联网控制网络摄像头，
出于安全原因，我想使用它，我总是在屋外和我的电脑连接，想不时地打开摄像头，以检查是否有问题！!"**

–[穆罕默德·萨利赫]

我们认为这是一个多么有趣的项目啊！以及许多不同的解决方法。休息之后看看我们对[Mohamed]的建议。

最初，我们想创建一个极其复杂的设置，使用 USB 摄像头、服务器、虚拟主机和大量脚本/编程来创建一个[相当不错的摄像头设置](http://www.aboutdebian.com/webcam.htm)。

但是，当然，复杂的面包问题，而挖掘我们的零件和用品箱，我们偶然发现了一个旧的[轴 206 IP 网络摄像机](http://www.axis.com/products/cam_206/)。还有什么比将上述所有功能集成到一个精巧的设备中更简单的呢！

相机配有一根以太网电缆、一个壁式电源和一张带有说明的 CD——我们只是扔掉了后者，通过找到如何重置设备及其默认 ip，我们很快就可以在我们的网络中看到相机。

一个简单的端口转发 80，我们可以在我们的网络之外查看它(只要我们键入我们的 IP)。然而，我们建议在网络内的一台计算机上建立一个 DNS ( [DynDNS](http://www.dyndns.com/) 很好)服务，指向摄像机 IP。这样，网址就变成了 http://www.HADCamera.com 的 T2，比 249.135.184.204:80 容易多了。(都是假网址抱歉)。

更进一步说，如果你附近有一台电脑，你可以设置一个简单的步进电机并[控制摄像机](http://hackaday.com/2010/01/07/spy-on-your-office/)的位置。

这当然是我们对此事的看法，Ask HackADay 的一部分是我们的读者会做的，那么你会如何设置家庭安全摄像头呢？