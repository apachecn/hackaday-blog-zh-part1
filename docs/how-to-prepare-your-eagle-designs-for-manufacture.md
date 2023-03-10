# 如何:为生产准备您的鹰设计

> 原文：<https://hackaday.com/2009/01/15/how-to-prepare-your-eagle-designs-for-manufacture/>

![back](img/4996dc880c4c7b5954079afa6202e0fc.png "back")

[Cadsoft Eagle](http://www.cadsoft.de) 是一款多平台免费软件电路布局程序。许多开源硬件都是在 Eagle 中设计的，它已经成为业余爱好者的最爱。我们将它用于我们所有的[硬件设计](http://hackaday.com/category/how-to/)。

有几种方法可以将 Eagle 设计变成实际的[印刷电路板](http://en.wikipedia.org/wiki/Printed_circuit_board) (PCB)。我们将向您展示如何将 Eagle 设计保存为任何 PCB 制造商都能接受的行业标准 gerber 文件。您可以使用 gerbers 订购单个原型或整个面板。

**简介**

墨粉转移是初学者最喜欢的制作 PCB 的方法，因为在材料上的投资是最小的。在之前，我们已经[介绍了墨粉转移。在我们的](http://hackaday.com/2008/07/28/how-to-etch-a-single-sided-pcb/)[指南](http://hackaday.com/category/how-to/)中，大多数 PCB 都是用[光阻工艺](http://www.ladyada.net/library/pcb/inhouseetch.html)制造的。照片处理可以制作漂亮的板子，但是需要一点设备；感光板、显影剂和紫外线光源。

一些电路板制造商，如 [Olimex](http://www.olimex.com/pcb/index.html) ，直接从 Eagle 生产 PCB。brd 文件。大多数要求最少订购一个[欧洲卡大小的](http://en.wikipedia.org/wiki/Eurocard_(printed_circuit_board))PCB(100 毫米 x160 毫米)。很好，如果你需要几个板，昂贵的单个实验原型。

最便宜的选择是像专业人士一样提交 [gerber 文件](http://en.wikipedia.org/wiki/Gerber_File)。任何 PCB 制造商都会接受 gerber 格式的设计文件。 [Gold Pheonix](http://www.goldphoenixpcb.biz/index.php) 出售 155 平方英寸的 PCB 面板，售价 110 美元。如果你正在寻找更小的东西，像 [BatchPCB](http://www.batchpcb.com/) 和 [PCB-Pool](http://www.pcb-pool.com/ppuk/info.html) 这样的服务将小订单组合起来，作为一个完整的面板提交。不管怎样，你都要把嘉宝的文件提交给董事会。这是我们描述的过程。

**流程概述**

*   准备设计。
*   创建 gerbers，任何 PCB 工厂都可以接受的通用文件。
*   验证 gerbers 是否正确。
*   将设计交付生产。

**准备设计**

我们将带您了解为生产准备我们的[数码相框](http://hackaday.com/2009/01/08/how-to-digital-picture-frame-100-diy/) PCB 的过程。这种设计需要一个走线相当小的双面电路板。

![eagle1](img/972b951d9b0f2ba768acdbfa97ac0846.png "eagle1")

下载上周的[项目档案](http://blog.mahalo.com/hackaday/howto/dpf.v1.zip) (ZIP)。打开。brd 文件与 [Cadsoft Eagle](http://www.cadsoft.de/freeware.htm) 的免费版本。

![eagle2](img/3316c22fa98172e33ebc6ce3cac213cb.png "eagle2")

文件打开时，地面填土为空。按下 ratsnest 按钮(*或工具- > Ratsnest* )来填充空的多边形。

![rules](img/b597db27f4e7678ac36e160d40b5a075.png "rules")

电路板制造商发布了概述其生产能力的规格，例如最小可能走线、间距和钻孔尺寸。BatchPCB 最小有 8 密耳[的走线和间距](http://www.batchpcb.com/index.php/Faq#What%20are%20the%20PCB%20rules%20and%20limits)，最小有 20 密耳的孔。

![pcb-justsayno](img/bc05398bb1e4aad1203c354182f73252.png "pcb-justsayno")

不要折磨厂家。只是因为他们宣传 8 密耳，并不意味着它是安全的，使每一个跟踪 8 密耳。稍大于最小公差将减少[制造误差](http://www.sparkfun.com/commerce/tutorial_info.php?tutorials_id=115)。数码相框在微小的 [LCD 连接器](http://www.sparkfun.com/commerce/product_info.php?products_id=570)周围有 8 密耳迹线，如上所示。走线只有 8 密耳，直到有足够的间隙使用 10 密耳走线。

![drc2](img/6409ddc5599657225a3d694b54fbe9b3.png "drc2")

使用 Eagle 的*设计规则检查*以确保您的主板不会超出制造商的生产能力。下载 BatchPCB 的 [SparkFun 设计规则](http://www.sparkfun.com/tutorial/Eagle-DFM/SparkFun.dru) (DRU)，或 Olimex [8mil](http://www.olimex.com/pcb/8mils.dru) (DRU)或 [10mil](http://www.olimex.com/pcb/10mils.dru) (DRU)设计规则。点击 DRC 图标(或者，*工具- > DRC* )并加载设计规则文件。Eagle 分析设计并突出显示任何违反设计规则参数的区域。

纠正任何错误。在这里，迹线之间的间距太近。有时，器件尺寸上的间距太小，无法制造。Sparkfun 的诺基亚 LCD 连接器的默认足迹的焊盘间距小于 8 密耳。我们[编辑了零件库](http://www.sparkfun.com/commerce/tutorial_info.php?tutorials_id=110)使焊盘变小，间隔变大。

![smash](img/dee39d080144ba3fead9aa50aef0e713.png "smash")

在印刷的丝印层上包含零件号很有帮助。BatchPCB 双面打印丝印。一定要看看你的寄宿公寓提供什么，有些是额外收费的。使用“粉碎”工具取消被遮挡标签的链接，然后将它们移动到更好的位置。

**创建嘉宝文件** 

Gerber 文件是 PCB 的[pdf](http://en.wikipedia.org/wiki/Portable_Document_Format)。Gerber 文件准确描述了 PCB 的外观，与显示硬件无关。这是最终的制作格式，不打算进行编辑。我们使用 [SparkFun 的 Eagle 教程](http://www.sparkfun.com/commerce/tutorial_info.php?tutorials_id=109)中概述的过程在 Eagle 中创建了我们的 gerber 文件。

![cam1](img/fabd4853e8af7aa94b954530a2a94d72.png "cam1")

Eagle CAM 处理器写入 gerber 文件，从菜单*文件- > CAM 处理器*下打开。

SparkFun 有一个[脚本](http://www.sparkfun.com/tutorial/BeginningEmbedded/9-EaglePCBs/sfe-gerb274x.cam) (CAM)，配置 CAM 处理器制作 gerber 文件。使用*文件- >打开- >作业…* 加载 CAM 脚本

![cam2](img/1b9c490d3d3ae96e40c019b5075fb9fc.png "cam2")

默认情况下，SparkFun 的丝印配置只包括 *place* 层。我们的零件通常在*名称*和 *docu* 层上有标签，激活顶部和底部丝印标签上的这些层，将它们添加到输出中。

点击*处理作业*创建 gerber 文件。

![files2](img/2ddea7f41aa96594e569b5e38bdbefdb.png "files2")

CAM 处理器创建了我们需要的七个文件。

*   顶部和底部铜(。GTL。GBL)
*   顶部和底部阻焊膜(。GTS。GBS)
*   顶部和底部丝网印刷(。GTO，。GBO)
*   钻孔文件，2.4 前导(。TXT)

**验证 gerbers 是否正确** 

在 [gerber viewer](http://www.mitsi.com/PCB/free%20viewers.htm) 中验证 CAM 输出，确保所有东西都放置正确。我们听从了 SparkFun 的建议，使用了[视图](http://www.viewplot.com/)。

![24leading](img/3373d6153dc6bee2aa4b1913b9982a1c.png "24leading")

用 Viewplot 加载这七个文件。*确保将钻孔文件类型指定为 2.4 前导。*

![viewplot1](img/b237c3a7dbc887043d7db6d7f39f2c56.png "viewplot1")

检查错误的过孔、镜像层和对准情况。我们注意到添加到丝网印刷层的文本通常比在 Eagle 中的要大。纠正任何问题，并再次运行 CAM 处理器。

当一切正常时，电路板就可以生产了。

**发送设计用于生产**

压缩七个 gerber 文件并提交给 PCB 工厂。*记得告诉他们 drill 文件格式是 2.4 leading。* ****

BatchPCB 是一个按平方英寸出售空间的共享面板服务。其他制造商和批量服务要求您至少向*订购*一张完整的欧洲卡。我们使用 BatchPCB 进行原型制作，因为我们从来不需要完整 eurocard 的额外电路板空间，而且我们不介意平均 20 天的等待。

在 BatchPCB，2.50 美元/平方英寸买一个两面都是丝印的 PCB，无限通孔，钻孔尺寸范围巨大；通常要额外付费的东西。BatchPCB 的最小走线、间距和钻孔与其他原型制作服务类似。每个订单有 10 美元*的安装费，但一个订单可以包括多个设计。航运，即使是国际航运，也不算离谱。*

如果你需要很多相同的板，看看金凤凰。他们为批量印刷电路板制造电路板。一个 100 平方英寸的面板是 100 美元，一个 155 平方英寸的面板是 110 美元。

![bpcb11](img/c14de9a154904185529e4ba9ff64b6d3.png "bpcb11")

在 [BatchPCB](http://www.batchpcb.com/) 创建账户。单击上传以添加新设计。命名设计并上传包含 7 个 gerber 文件的 zip 存档。

![bpcb2](img/8422bf62bfab468a392b9634515ad7c7.png "bpcb2")

验证是否成功检测到 gerber 层。

![bpcb3](img/90172221552530296df2a1fef2ea84e5.png "bpcb3")

验证是否检测到正确的大小。

![bpcb4](img/9792015bfccc21807959c1954ab7e94b.png "bpcb4")

BatchPCB 规则检查“机器人”将验证您的设计是否符合生产标准，并在几分钟内发送电子邮件。由于我们在发送设计之前运行了我们自己的规则检查，我们可以预期一切都会好的。单击继续，您将可以选择订购主板。更多帮助，请参见 BatchPCB [帮助](http://www.batchpcb.com/index.php/Help)和[支持论坛](http://www.sparkfun.com/cgi-bin/phpbb/viewforum.php?f=16)。

**接收您的电路板**

**![boards](img/7fff7343df4a3de629433d8d3c27f096.png "boards")
**

电路板大约在 20 天内从批次 PCB 到达。焊接前检查电路板是否有明显的错误。有些厂家测试 PCB，BatchPCB 不测试。我们已经从两个受欢迎的业余爱好者电路板公司 Olimex 和 BatchPCB 订购了 PCB，所有的电路板都令人满意。

**更进一步**

使用 gerber 文件很容易订购专业 PCB。为什么不去做你一直推迟的那个很棒的 DIY 项目呢？

你对 PCB 工厂有什么经验？

更新:文件已被移动！[在这里找到他们](http://www.whereisian.com/files/dpf.v1.zip)。