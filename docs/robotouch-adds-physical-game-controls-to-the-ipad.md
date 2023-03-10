# RoboTouch 为 IPad 增加了物理游戏控件

> 原文：<https://hackaday.com/2011/03/16/robotouch-adds-physical-game-controls-to-the-ipad/>

![robotouch](img/9f2ef0ce7ae8d7cf8066157557a2dd13.png "robotouch")

[ProtoDojo]想在他的 iPad 上玩一款赛车游戏，但他不太喜欢使用这款游戏的触摸界面。相反，他组装了一个非常简洁的小程序，允许他用一个旧的 NES 控制器在 iPad 上玩游戏。

他建造了一套定制的导电臂，安装在三个微型伺服系统上。伺服系统是用小吸盘固定在 iPad 屏幕上的，吸盘位于预期接受按钮按压的位置。它们还被连接到一个 Arduino，该 Arduino 解释来自所连接的 NES 控制器的按钮按压。当 Arduino 感觉到 D-pad 或按钮被按下时，它会触发伺服系统，进而按下屏幕上的虚拟按钮。

在下面的视频中，你可以看到调整伺服位置后，设置似乎工作得很好。您可能希望看到这样的设置有一些延迟，但是我们没有注意到任何延迟。[ProtoDojo]网站目前因流量过大而关闭，但是一旦它恢复运行，您应该可以在那里找到更多的构建细节。

[https://www.youtube.com/embed/c9u87WPhVK8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/c9u87WPhVK8?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)