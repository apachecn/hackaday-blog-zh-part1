# snes 游戏手柄转换为 usb

> 原文：<https://hackaday.com/2011/09/25/snes-gamepad-coversion-to-usb/>

![](img/1f7bba52dae41b4e2654c93d540e6eff.png "snes-gamepad-for-android")

[Kekszumquadrat]想要使用经典控制器在他的 Android 平板电脑上玩模拟器游戏，所以他开始将 SNES 游戏手柄转换为通过 USB 连接。他在旧货市场发现了一个旧的 USB 键盘，价格约为 3 欧元。他知道他喜欢的仿真器可以将所有输入重新映射到键盘按键，这意味着 USB 键盘拥有他完成这项工作所需的所有电子设备。

一旦他将键盘电路从机箱中分离出来[Kekszumquadrat]将其插入他的 Linux 盒子中，并使用 Xev 来建立键盘矩阵的设置方式。Xev 是一个在 X 桌面上打开活动窗口的通用包。当从命令行运行时，窗口中发生的任何事件都将与该事件的详细数据一起回显。说到按键，你会得到你需要的键码。他只是简单地缩短列和行，直到他找到所需的映射，然后就可以焊接了。

SNES 控制器是非常简单的设备。正如我们在之前的项目中看到的[，他们使用串行到并行移位寄存器来收集按钮数据并将其发送到控制台。[Kekszumquadrat]简单地焊接在按钮走线和键盘矩阵触点之间。一旦他完成了，键盘部分被塞进控制器盒里，他留下了一个 USB 控制器，似乎没有改变。](http://hackaday.com/2011/09/08/arcade-controller-in-a-box/)