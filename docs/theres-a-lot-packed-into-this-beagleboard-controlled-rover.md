# 这个由猎兔犬控制的探测车上装了很多东西

> 原文：<https://hackaday.com/2011/11/14/theres-a-lot-packed-into-this-beagleboard-controlled-rover/>

那个黑匣子里藏着各种各样的好东西，这让这辆漫游车成为了黑客乐园。[Andrey]围绕 BeagleBoard 构建了该设备，beagle board 提供了他需要的处理能力和模块，以使其余部分工作。

控制单元将飞行员缩小到火星车的大小，使用一个有方向盘和其他控制装置的驾驶舱，以及一个播放来自机器人前面摄像头的视频流的监视器。它有一个 WiFi 适配器，可以通过互联网进行控制。由于其伺服安装，摄像机可以旋转，将视频传输到 BeagleBoard，在那里使用 h264 编解码器进行压缩(更多信息请参见[和驾驶舱，此处为](http://veter-project.blogspot.com/2011/11/how-to-build-beagleboard-based-wifi.html))，以减轻流媒体负载。你还会在前面找到一个超声波测距仪用于避障，一个磁罗盘用于方位信息。最后，GPS 支持这些数据，允许你在地图上描绘你的冒险。

这很棒，但会让你付出代价。材料估价超过五百欧元！