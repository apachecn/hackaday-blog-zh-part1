# 假 PS3 一路跟踪小偷回家

> 原文：<https://hackaday.com/2011/09/30/fake-ps3-tracks-thieves-all-the-way-home/>

![ps3_tracking_system](img/d2b3b4c9e484932bbb407a67f3a37ee6.png "ps3_tracking_system")

[Wayne 的]一个亲戚的房子在暴风雪/长时间停电期间被盗，通常情况下，没有一件被盗物品被找回。他侄子的 PS3 在被盗物品中，这让他很不舒服。受警方“诱饵车”的启发，他认为在虚拟游戏机上安装一个跟踪装置会很酷，如果将来有类似的事情发生。

他在易贝买了一个挖空的 PS3 外壳，里面填充了一个 Arduino、一个加速度计、一个 GPS 传感器、一个带有预付费 SIM 卡的小型 GSM 调制解调器和一个大小合理的 LiPoly 电池。该系统通常处于睡眠状态，但当加速度计感应到运动时，Arduino 会启动 GSM 调制解调器，并向他的手机发送短信安全警报。通过手机短信控制追踪系统，他可以请求 GPS 坐标和方向信息，这些信息可以传递给警方。

他的追踪系统是个好主意，因为贩卖偷来的游戏机对小偷来说很容易赚钱。如果你的邻居碰巧发生了一连串的抢劫案，你当然可以稍微放心一点，因为你的 Playstation 二重身会让你知道有人正在抢劫你的房子。