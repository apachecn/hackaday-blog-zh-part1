# 线环游戏通过收缩你的魔杖来惩罚触摸

> 原文：<https://hackaday.com/2012/02/17/wire-loop-game-penalizes-for-touches-by-shrinking-your-wand/>

![](img/ab578c9573aeddfd568090920150aee4.png "Xtreme-Buzzwire-4-2-Arduino-Jam-project")

我们真的很喜欢[这款采用导电钢丝的迷宫游戏](http://www.instructables.com/id/Xtreme-Buzzwire-4-2-Arduino-weekend-project)。这是比利时 48 小时黑客马拉松的成果，该活动要求所有源于该活动的项目都使用 Arduino。我们认为[Jan]和[Kristof]在规定的时间内完美地利用了原型装置。活动组织者也这么认为，因为这获得了最高奖项。

正如你所看到的，游戏区是双面的，由一些弯曲成迷宫的铜线组成。有一根 PVC 管制成的魔杖，有一圈编织电缆穿过它。这个环围绕着铜轨道，每个玩家都需要从起点到终点，在不接触轨道的情况下触摸沿途的检查站。

很标准，对吧？有个转折。在每个检查点，Arduino 都会向棒中的伺服电机发出信号，使线圈变小。除此之外，还有一个惩罚/奖励系统:如果你接触轨道，你的圈变小，而你对手的圈变大。休息之后不要错过头对头的动作。

这让我们想起了几年前的那场钢索洞穴赛车。T3[https://www.youtube.com/embed/T8CjX9vgBoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/T8CjX9vgBoE?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[谢谢卡通]