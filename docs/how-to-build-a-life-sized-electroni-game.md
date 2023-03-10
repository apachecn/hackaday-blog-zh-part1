# 如何建立一个真人大小的电子游戏

> 原文：<https://hackaday.com/2009/09/12/how-to-build-a-life-sized-electroni-game/>

![life_size_light_games](img/a3661632ff137e54860fe300ac27b694.png "life_size_light_games")

我们对史蒂夫的电子打雪仗游戏印象深刻。它由两个真人大小的玩家面对面站着组成。每人可以扔一个雪球或鸭子，目标是击中对方，而自己不会被击中。他利用了许多好的构建技术，可以很容易地适应其他类型的游戏。

![lights_in_place](img/f734c2b4aa672134be9af4cee92200a1.png "lights_in_place")

对于球员的轮廓，[史蒂夫]拍摄了他自己站立、躲避和投掷动作的照片。每张照片都被用来生成一个轮廓，然后被印刷到某个泥瓦匠上。然后，他沿着轮廓钻了几个洞，并把圣诞灯放了进去。一根弦用于一个电路。

![SSR_module](img/c42ac23cba6ccb786336a351fbc22276.png "SSR_module")

一个固态继电器板被用来控制灯串的开关。[Steve]将它放在一个不受天气影响的实用程序箱中，并使用延长弦来方便连接灯。使用 CAT5 以太网电缆将 [SSR](http://en.wikipedia.org/wiki/Solid_state_relay) 连接到控制器。控制器是一个 Arduino 和一个 595 端口扩展板，为游戏提供足够的输入/输出引脚。

![controls_and_scoreboard](img/3a987e4709cf862b2795ea3313d05d55.png "controls_and_scoreboard")

这个项目的两个令人愉快的创造性部分是按钮和记分牌。按钮是根据游戏的规模制作的。[史蒂夫]拿起四个用过的按钮式灯，接入它们的瞬时按钮开关，加上 LEDS 反馈。对于记分牌，他使用反光胶带和 led 以及泡沫边框来创建 7 段显示。

计划周密，执行良好，是一个全方位的伟大建设！不要错过我们在下面嵌入的[Steve]逐步解释视频。

[https://www.youtube.com/embed/hlOorpY55SA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/hlOorpY55SA?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)