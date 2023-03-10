# Android 手机作为 Arduino 终端

> 原文：<https://hackaday.com/2011/09/13/android-phone-serves-as-arduino-terminal/>

![](img/e757602d86faed62bcd8d4527f0e2772.png "use-android-device-as-arduino-terminal")

为了在旅途中使用他的 Arduino，[Oleg]一直在研究一种方法来使用 Android ADK 终端模拟器和 Arduino。Android 端使用 ADK 功能和一个定制应用程序。[Oleg]在为 Android 开发程序时得到了他的朋友[Victor]的帮助(如果你有兴趣了解这是如何完成的，你可以查看我们自己的 [Android 开发教程](http://hackaday.com/2010/07/15/android-dev-101-%E2%80%93-part-1hello-world/))。的。apk 文件可供下载，但他们正在等待发布源代码，直到他们可以清理它，并从测试版中获得一些棘手的错误。

Arduino 的 USB 主机护罩需要连接到 Android 手机。您将能够通过终端发送和接收字符串，并支持回车和换行字符。不幸的是，这不允许你改变、编译或写草图到 Arduino。但是当电脑不在的情况下解决项目问题时，或者只是使用 Android 手机作为输出时，它可能会非常方便。