# WiFi 流媒体收音机

> 原文：<https://hackaday.com/2008/12/19/wifi-streaming-radio/>

![wifiradio](img/631467f604dd12bd53cda899e2b10f75.png "wifiradio")

[杰夫]正在继续他的 [WiFi 流媒体广播项目](http://mightyohm.com/blog/2008/10/building-a-wifi-radio-part-1-introduction/ "mightyOhm  » Blog Archive   » Building a Wifi Radio - Part 1, Introduction")，现在进入[第七部](http://mightyohm.com/blog/2008/12/building-a-wifi-radio-part-7-building-an-lcd-display/ "mightyOhm  » Blog Archive   » Building a Wifi Radio - Part 7, Building an LCD Display")。之所以花了这么长时间，是因为他费心记录系统的每一个部分，而不是假设太多的读者。该系统的核心是华硕 WL-520GU 无线路由器。它由 [OpenWRT](http://openwrt.org/ "OpenWrt") 支持，并有一个 [USB 端口](http://www.mahalo.com/USB "USB - Mahalo")用于外部声卡。 [mpd](http://mpd.wikia.com/wiki/Music_Player_Daemon_Wiki "Music Player Daemon Community Wiki") ，音乐播放器守护进程，用于播放。这一最新部分的特点是为当前曲目添加了一个 LCD 显示屏。路由器板已经有了串行端口的点，所以只需添加一个 AVR 来与 LCD 对话。下一步是构建一个简单的用户界面，然后将所有东西打包。您可以观看下面显示的视频。