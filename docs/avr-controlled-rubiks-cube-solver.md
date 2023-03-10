# AVR 控制的魔方解算器

> 原文：<https://hackaday.com/2009/09/11/avr-controlled-rubiks-cube-solver/>

[https://www.youtube.com/embed/ThMd9YR1MAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/ThMd9YR1MAg?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)

[安德留斯]刚刚派出他的机器人[魔方解算器](http://sutas.lt/rubiks-cube-solving-robot-rdrk/)。它没有我们去年看到的[解算器](http://hackaday.com/2008/11/23/cubear-berkeleys-rubiks-cube-solver/)快，但也不需要那么多部件。这个项目使用了两个爪子，每个爪子仅由两个伺服电机驱动。这种思考是由电脑完成的，电脑会计算出解决魔方的必要步骤。然后，每个指令通过 USB 传输到负责伺服操作的 AVR ATmega16 微控制器。

现在看来，在计算解决方案之前，必须手动输入每个起始面的颜色。我们认为[安德留斯]可能正计划用他的下一代软件来升级它，因为他已经为这种类型的分析设置了一个网络摄像头。