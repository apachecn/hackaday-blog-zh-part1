# Android 上的 WiFi 和蓝牙共享

> 原文：<https://hackaday.com/2009/02/10/wifi-and-bluetooth-tethering-on-android/>

![tmobileg1](img/50dd2c797a0c9b418c2209459ae06ff5.png "tmobileg1")

许多 G1/ADP1 用户一直在使用应用程序 [Tetherbot](http://graha.ms/androidproxy/ "Tetherbot") 通过 [USB](http://www.mahalo.com/USB) 与手机的数据连接，在他们的[笔记本电脑](http://www.mahalo.com/Laptop_Hacks)上接入互联网。该应用依赖于 [Android 调试桥](http://code.google.com/android/reference/adb.html "Android Debug Bridge - Android")来转发端口。这很有效，但是人们想要一个比 SOCKS 代理更好的解决方案。社区想出了一种方法，使用 iptables 创建一个正确的 NAT 连接，然后[moussam]将它们整合成易于使用的应用程序。一个用于在蓝牙上设置 [PAN 设备，另一个用于](http://androidactivity.com/ "Android G1 Bluetooth tethering - Android Activity")[临时 WiFi 联网](http://androidactivity.com/tetherWifi.html "Android G1 Wifi tethering - Android Activity")。它要求你的手机有 root 权限，但希望你已经做到了，并且已经运行了最新的社区固件。

[照片: [tnkgrl](http://flickr.com/photos/tnkgrl/2963841190/in/set-72157608262752711/)