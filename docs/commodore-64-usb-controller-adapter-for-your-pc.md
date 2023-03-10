# 适用于您电脑的 Commodore 64 USB 控制器适配器

> 原文：<https://hackaday.com/2011/07/31/commodore-64-usb-controller-adapter-for-your-pc/>

![commodore_64_controller_usb_interface](img/5a4e748f8b0fdac95e7237d2204d65bf.png "commodore_64_controller_usb_interface")

[弗兰克]和许多人一样，对 64 号准将情有独钟。如今，他更喜欢在自己的电脑上玩 C64 游戏，但更喜欢用他以前学校的竞赛职业选手 T1，而不是一些重新映射了按钮的现代控制器。使用控制器的唯一问题是，他的新电脑没有任何端口来容纳其 9 针 D-sub 连接器。

VICE emulator 将键盘输入映射到控制器动作，因此他决定为自己构建一个实现虚拟 USB 键盘的 D-sub 转 USB 适配器。他为 Freescale MC9S08JS16L 微控制器编写了一个固件包，允许他在使用 Competition Pro 操纵杆执行某个操作时向仿真器发送按键。

该电路看起来比我们之前见过的一些其他 C64 接口更容易复制，正如你在下面的视频中看到的，它工作得相当好。我们设想这种设置可以用来将各种旧的输入设备连接到现代个人电脑上，几乎不需要调整。

[https://www.youtube.com/embed/SkqbnitMFDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/SkqbnitMFDk?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)