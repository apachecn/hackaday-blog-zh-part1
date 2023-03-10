# 太空相机在飞行中传输数据流

> 原文：<https://hackaday.com/2011/09/19/space-camera-streams-data-during-flight/>

![](img/1a6a8a706f3f9084381cb6e50e8e545e.png "payloadtotal")

通过在飞行期间传输数据，冒着无法从近空间相机发射中恢复硬件的风险。[Tim Zaman]是开发上述装置的团队成员之一。在最近的气球发射中，它发回了 119 张图像。这包括高达 36 公里的传输。

主要硬件包括一个装有网络摄像头的比格犬板，放在一个聚苯乙烯泡沫冷却器中用于热保护。将它与用于位置跟踪的 GPS 模块和用于数据传输的 GPRS 模块配对，您就可以开始工作了。

但这还不是上涨的全部。该团队建立了一个备份硬件模块，以防主模块出现故障。这辆车也有 GPS 和 GPRS 无线电，但由 Arduino 驾驶。

无线电连接使得恢复硬件变得容易。全球定位系统的数据直接引导团队到达着陆点。包裹停在了一栋建筑的屋顶上，但我们猜想这比挂在一棵大树顶上更方便。

不要错过休息后我们嵌入的硬件细节视频。

[https://www.youtube.com/embed/2jlkxkstruI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/2jlkxkstruI?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)