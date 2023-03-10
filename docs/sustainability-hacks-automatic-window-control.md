# 可持续发展秘诀:自动窗户控制

> 原文：<https://hackaday.com/2011/09/29/sustainability-hacks-automatic-window-control/>

![](img/bb77d6f9b7260f9a40b0b5acb939dd2a.png "Sustainability Hacks")

![](img/45f2859e8d1e38cad364f99677b84b8c.png "window")

有时候，改变一个小小的绿色黑客会让它变成一个和我们的游戏装备一样浪费能量的建筑。[韦斯特博士]的[自动窗户控制器](http://afrotechmods.com/forums/index.php/topic,8830.0.html)就是其中之一。好消息是，窗户控制器可以很容易地修改，以减少秋季和春季的能源成本。

[韦斯特博士]对他公寓里的温度没有任何控制，在整个加拿大的冬天，他的公寓变得非常热。他不付取暖费，所以他做了我们任何人都会做的事情——打破窗户。受这篇文章的启发，他在厨房的窗框上安装了一个[线性致动器](http://i29.photobucket.com/albums/c275/Omgusername1/Window%20thermostat/window.jpg)。[韦斯特博士]不想损坏窗框，所以他将致动器连接到一块方形铝管上，铝管安装到现有的螺丝孔上。

电子方面，West 博士]使用了一个 [Rabbit 2000](http://www.rabbitsemiconductor.com.cn/products/rab2000/index.shtml) 开发板、LCD 显示屏和键盘，并在一块试验板上构建了一个 H 桥电路。由于端口冲突和公认的懒惰，Arduino 被用来读取热敏电阻。显示屏显示当前和期望的温度，兔子相应地打开和关闭窗户。所有的源代码都贴在论坛的帖子里。

虽然将建筑物 HVAC 系统的热量排放到冰冻的苔原上并不是最“绿色”的想法，但这将是在更温和的季节自动打开和关闭窗户的一个很好的构建。白天打开窗户，晚上关上窗户，你回家时不会再有太热或太冷的问题。休息之后来看看自动窗口的视频。

[https://www.youtube.com/embed/Mv40UBkajDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/Mv40UBkajDc?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)