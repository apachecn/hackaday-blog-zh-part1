# 遥控机器人坦克

> 原文：<https://hackaday.com/2005/04/02/telerobotic-tank/>

![telerobotic tank](img/c8ab2b2a33304a12c5273c77ff3c7764.png)

“T0”火星漫游车“T1”是一个由机器人爱好者 kerwin lumpkins 制造的远程呈现机器人。他创造了一个真实的火星漫游者的模型，但规模更实际。

控制坦克的是通用机器人开发板，也是 kerwin 设计的。 [darc 板](http://www.ranchbots.com/DARC_board/darc_board.htm)从红外和声纳传感器获取输入，控制移动和相机瞄准，并具有根据其周围环境和操作员命令的组合做出决定的基本能力，这些命令通过 rf 调制解调器连接发送给机器人。

这就是它的酷之处。如果机器人检测到给定的命令将处于危险中(例如撞上厨房橱柜)，它将中止并向控制站发回警告。

为了更好地模拟真实的火星漫游系统，kerwin 使用一些类似 tivo 的时移软件将输入的视频信号延迟 5 秒。这使得控制火星车变得更加困难，这也是为什么星上决策对于你自己的火星探测器项目来说是必须的。

*   [永久链接](http://www.ranchbots.com/mars_rover/rover.htm)