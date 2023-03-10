# 间谍视频追踪:拆卸

> 原文：<https://hackaday.com/2010/08/30/spy-video-trakr-the-teardown/>

![](img/f712d1fe7a9d5092f616967657e72f9d.png "trakr-closeup")

上周五[我们主要从最终用户的角度看了野生星球的间谍视频 TRAKR](http://hackaday.com/2010/08/27/spy-video-trakr-first-impressions/) 可编程遥控车辆。为了更好地衡量 TRAKR 的真正黑客能力，我们周末的大部分时间都花在了拆卸和拍摄设备的内部工作，以及钻研代码和文档上。我们之前的审查包括一些错误的猜测…我们现在可以澄清一些细节，并继续推进完全*新*错误的猜测！

我们这次拆解的计划是建立更多具体的细节，说明设备内部哪些是可以黑客攻击的，哪些是不可以的，并帮助确定一些未说明的硬件规格。

我们错误地报告说还没有可用的编程文档或编译器。原来所有这些信息都简单地藏在 TRAKR 网站的[帮助部分，而不是我们期望的“App BUILDR”页面。*德尔普！*这些资源仍处于粗糙状态，但已被证明是比物理拆卸更有价值的信息来源。尽管 c 代码和 pdf 不是很](http://www.spygear.net/help/apps.php)[上镜](http://hackaday.com/2010/08/29/art-piece-from-board-artwork/)，所以我们有足够的电路板 pr0n 开始！

## 遥控器内部

在 TRAKR 遥控器里没有那么多可看的或可做的，所以我们将先浏览一下。

![](img/319bfddccccb72160ca4951942e7c7bf.png "remote-usb")

上次提到了隐藏的后部 USB 端口，我们被告知这是为了允许现场升级固件。如果你不介意被拴在一个点上，我们发现遥控器也可以通过 USB 集线器供电，甚至可以通过 TRAKR 自己的 USB 主机端口供电。

在另一个对修补者友好的设计中，遥控器和 TRAKR 都用完全相同的 Phillips 螺丝固定在一起，凹进但不隐藏在贴纸或橡胶垫下。

![](img/4c2317dde750e53df4596e7e79df94d7.png "remote-internals")

LCD 屏幕是手机中常见的屏幕，15 位彩色，160×120 像素。

![](img/ddcc96b83ce3ae6dc0cfcafe6e658341.png "remote-switches")

“机器人开关 PCB”只有一些开关和无源元件。SW1 和 SW4 有专门的用途(主菜单和电源)，但其他功能由单独的应用程序定义。如果你正在寻找 GPIO 线路来入侵遥控器，这可能是你最好的选择。

![](img/82bbddc0b93030c825f9a57a6b1c0e31.png "remote-pads")

The underside of the main remote PCB has some exposed pads, but there are no through-hole solder points. The pad labeled “V0_TVOUT” caught our attention, thinking it might provide a [composite video signal](http://hackaday.com/2010/06/30/didj-composite-video-out/), but this turned out not to be the case, or at least it’s not enabled in the present firmware. J9 looks like a [JTAG](http://hackaday.com/2009/06/25/how-to-the-bus-pirate-v2-with-usb/) header.

![](img/3f808cfea8f62ad0d5ddc4b8b999b8e5.png "remote-morepads")

LCD 下面还有几个测试点。

![](img/1798e99a2b8f70fbcdc4722eb973a3d4.png "remote-mem")

远程 2 兆 SDRAM 和 1 兆 SPI 闪存。

![](img/15c9b04f3b60ba8f985d618c1e09d5b8.png "remote-stick")

我们真的希望操纵杆内部是模拟的，但没有这样的运气…它们只是简单的前进/后退开关。即使用电位计替换，如果不访问固件源，也无法将此信息传递给 TRAKR。

![](img/1084bb4b56e0fa20b0600007ef0dea74.png "remote-wireless")

遥控器和跟踪器具有外观相同的无线电收发器。它们密封得相当好，我们还没有进一步拆卸它们，但记得听说它们基于北欧 2.4 GHz 器件。Wild Planet 声称，随着即将到来的固件更新，它们将具备 WiFi 功能。我们仍然充满希望，但也持怀疑态度——遥控器后面的 USB 端口似乎更有可能发挥作用，或者在此期间，也许 [SparkFun Nordic 选项中的一个](http://www.sparkfun.com/commerce/product_info.php?products_id=151)将被证明是 PC 控制的可行选择。

## 在轨道内部

![](img/28858e17e6be2d5bf065635d7e045dfb.png "trakr-cables")

卸下螺丝很简单，但要将盖子从 TRAKR 上完全卸下来，需要先卸下几根电缆——为了可靠起见，它们都被粘在了合适的位置。我们只是用 X-acto 刀切开胶水，撬开一点，但也许它可以更微妙地溶解或融化。

![](img/1593d2cfbd502d6356ac6e9682d6ec67.png "trakr-pcb1")

主板的右侧(此处转向侧面)关注连接和 CPU。左边的带状电缆通向摄像机。这对两针接头通向麦克风和前附件碰撞开关。无人使用的 SW1 的用途不得而知——它可能是早期设计的一个额外的后部或顶部开关，现在已经退化了。较大的头部通向无线电模块和微调电位计以及机器人底盘上的凹进复位/调试开关。

不需要穿过环氧树脂。通过挖掘编译器的配置文件，该芯片似乎是一个 Nuvoton [W55VA91](http://www.nuvoton.com/NuvotonMOSS/Community/ProductInfo.aspx?tp_GUID=97c1dcb2-17d8-4bb8-bd40-28c98a3a58b0) ，具有一个运行在 192 MHz 的 ARM926EJ 内核和硬件辅助 JPEG 编解码器。

![](img/1445845a67cd2a6c0f768042fde2eeb7.png "trakr-pcb2")

棋盘的中间部分是 TRAKR 黑客最熟悉的部分。JACK3，中间垂直排列的焊盘，包含 8 条数字 GPIO 线和一个模拟输入，引脚间距为 0.1 英寸。JACK4 看起来像一个 JTAG 端口，引脚间距为 2mm。下面是 USB 主机端口的连接器，右边的第二个(未安装的)端口可以用作 5V 电源。非常遗憾的是，JACK3 上的电源和接地被忽略了，尽管它靠近这些迹线。加上电源走线和焊接到位的行式接头，这将成为小型附加设备的一个很好的标准化 riser，很像已经起飞的 Arduino " [shields](http://hackaday.com/2010/07/01/arduino-webserver/) "生态系统。

![](img/528eccb4a0cb116d2c45cf07be1c932f.png "trakr-pcb3")

电路板的左侧主要用于电源和电机控制。左边的红/黑线通向电池盒。上面的连接器是扬声器用的。底部的两个 3 针连接器通向左右电机，上方是 H 桥驱动电路。

顺便说一下，如果你拆卸了你的 TRAKR，当需要把它装回去的时候，有四个螺丝孔实际上并没有被使用，尽管它们在丝印层上有标签。你可以在上面的照片中看到其中的三个，第四个在相机连接器附近的前一张照片中。强行拧入螺钉可能会损坏下面的一根电机电缆！

![](img/ca17986772a4c0d7ca76ccca604214f5.png "trakr-pcb-bottom")

下面几乎看不到。又一个不活跃的 V0_TVOUT pad 嘲讽我们！这一面主要是由 SD 卡插座，和…

![](img/fb6d57b30ba7a70c9453dc2e9c2a01b9.png "trakr-mem")

…ample 8 megabyte SDRAM, 2 megabyte flash. Together with the SD slot, USB and ARM9 CPU, we’re anticipating [ucLinux](http://hackaday.com/2007/08/30/uclinux-based-embedded-asterix-pbx/) and [DOOM](http://hackaday.com/2010/06/21/psp-homebrew-using-the-half-byte-loader/) to be ported in 3…2…1…

![](img/c71ee55893974fc5e8497a2486e617bb.png "trakr-pcb-misc")

USB 主机端口在一个小子板上，每个电机也有一些本地驱动电路。

![](img/045638db7d2195dd44054a31a1824e96.png "trakr-gearbox")

每个电机通过减速[齿轮箱](http://hackaday.com/2010/04/08/lego-gearbox-seven-speed-plus-reverse/)驱动。它们安静地运转，只有少量的污水。至于收音机，我们还没有进一步拆除这些。

![](img/633fdc4ecef132033110da3ee04a27ae.png "trakr-spring")

虽然没有动力，前轮并不像我们最初想象的那样无聊。这种齿条和弹簧机构使橡胶胎面带保持恒定的张力，当 TRAKR 在各种地形上行驶时，允许它们弯曲并保持牵引力。

![](img/683870cb2e85d8627abf4a74f4bf0407.png "trakr-camera-slide")

部分拆卸的相机枢轴机构。两个小橡胶垫提供了足够的摩擦力来将相机固定在设定的位置，但仍然允许它轻松地旋转。如果试图将[伺服控制](http://hackaday.com/2010/07/18/servo-controller-board/)添加到相机中，移除这些衬垫可能会有所帮助。

摄像机通过一根 24 芯柔性电缆连接到主印刷电路板上，电缆间距为 0.5 毫米，长约 6 英寸。将相机安装在更高的位置可能最好是用更长的电缆替换整个电缆，但我们尚未从 DigiKey 等来源找到合适的匹配。

![](img/efe4a6e4f48714cd30e7cb8aadc08d5a.png "trakr-camera-leds")

从外壳中取出相机 PCB 时，迎接我们的是一个唾手可得的机会:电路板的设计可以容纳多个 led，但实际上只安装了一个大的。[增加光输出](http://hackaday.com/2010/03/17/woot-how-to-let-there-be-light-for-your-rovio/)应该是一件非常简单的事情，增加缺失的电阻和 led，尽管你需要在外壳上钻孔或布线以从外部安装 led。

我们还不能 100%确定摄像头传感器。从 Maker Faire 的公关材料中，我们知道它来自 OmniVision，但不知道确切的型号。基于尺寸和规格，OV7670 看起来像是一种可能性，在这种情况下，*应该*能够实现全 VGA 分辨率，而不仅仅是我们看到的 QVGA 输出。

![](img/c845d29122763c0ca186f655ca9d75ac.png "trakr-accessory")

“附件端口”只是一个被动的连接点，用来夹东西；它类似于耳机插孔，但不是。它后面有一个按钮开关，可能是一个交互式的戳猫棒。

![](img/5f2f0320d856f70dececaa8ff4afb6c1.png "trakr-name")

艺术家的签名。

重新组装很简单。电缆连接器的方向是键控的，对于那些没有唯一尺寸的连接器，可以从电缆长度推断出正确的位置。而且最后没有神秘的“额外螺丝”——所有东西都很容易地组合在一起，并且在第一次尝试中就成功了。

## 乘客

Some readers have asked about [mounting external microcontrollers](http://hackaday.com/2010/03/05/rc-truck-source-for-robotics-platform/) or other devices to the rear transport deck. Adding a microcontroller isn’t an entirely ridiculous prospect — even though the TRAKR’s CPU has far more “oomph,” it remains to be seen if the GPIO lines are suited to tasks such as accurate [PWM](http://hackaday.com/2009/09/17/software-pulse-width-modulation/) for servo control. Delegating such tasks may prove helpful, or even necessary. The usable area of the transport deck is a bit over five inches wide and three inches deep, and a couple of rubber bands or some foam tape will hold most boards securely. With the deck removed, the recessed notch above the battery bay is such a perfect size for certain things, it’s almost uncanny. Did [Dave] plan this?

![](img/6aa4d4b28730605ec1b27bdabbfbcbca.png "trakr-back-arduino")

阿尔杜伊诺，当然。像这样的小设备可以从 TRAKR 的 USB 主机端口供电，但如果主机端没有 [FTDI](http://hackaday.com/2009/09/22/introduction-to-ftdi-bitbang-mode/) 驱动程序，这种连接就不能用于串行通信。

![](img/054ad9141c1c08358076586cc3a50751.png "trakr-back-breadboard2")

半尺寸和四分之一尺寸的试验板非常合适，几乎可以咬合到位。但是放在这里的任何东西都会阻挡对 SD 和 USB 端口的访问。

## 更多黑客想法

从里到外探索了硬件之后，我们已经在思考各种可能性…

TRAKR 的前面有一个大的红外 LED(两个更容易添加)。 [TV-B-Gone](http://hackaday.com/2009/08/17/adafruit-releases-new-tv-b-gone-kit/) 的固件是开源的。说够了。

![](img/d3b53c9804f0e3b79b5799e7438a3ba4.png "trakr-segway")

卸下运输平台后，TRAKR 的后轮稍微突出到车身后面。随着陀螺传感器的加入，是否有可能让 TRAKR 直立起来，并像赛格威那样四处滑行？遥控器的操纵杆是非比例的，但是马达的软件控制允许非常精细的速度调节。这是用乐高 NXT T3 完成的[，所以我们认为这个想法的实用性将取决于 TRAKR 马达的响应能力。(是的，我们*知道*它就支在那里的后墙上。*嘘！*)](http://hackaday.com/2009/04/21/wii-controlled-segway-style-nxt-bot/)

![](img/ff62d905f5b9ea385737f1d39ca5fc48.png "trakr-pov")

TRAKR 的宽姿态让我们考虑一个 [Chalkbot](http://hackaday.com/2009/07/09/chalkbot-vs-graffitiwriter/) 或 [txtBomber](http://hackaday.com/2010/08/05/txtbomber/) 打印机附件:八条 GPIO 线可以用来控制连接到油漆标记器或粉笔灰斗的一排[螺线管](http://hackaday.com/2010/02/17/robo-vibe/)。我们手头没有部件来立即建造一台物理打印机，但我们确实有一些来自另一个项目的[可寻址 LED 条](http://hackaday.com/2010/05/31/beginner-concepts-cascading-shift-registers/)，所以使用[长曝光摄影](http://hackaday.com/2009/12/02/worlds-largest-pov-display/)进行概念验证是可能的。而且*管用！*当我们接触到 TRAKR C 编译器时，我们将在后续的文章中详细阐述这个技巧。