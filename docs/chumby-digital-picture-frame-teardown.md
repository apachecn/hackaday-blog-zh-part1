# Chumby 数码相框拆卸

> 原文：<https://hackaday.com/2009/01/20/chumby-digital-picture-frame-teardown/>

![overview-1](img/ff72c7352bd5a8a9856c372716cdd6f7.png "overview-1")

在今年的消费电子展上， [Chumby](http://www.chumby.com/ "chumby internet radio player, digital picture frame, alarm clock - more!") 展示了他们的最新原型。这是一个联网的数码相框，运行 Flash 小工具。就像现在的 Chumby 模型一样，他们发布软件和硬件的许可证是为了让你破解它。他们让我们借用他们的开放式机箱评估套件进行拆卸和拍照。我们有更多的图片，完整的规格，和下面的原理图。

![boot](img/b78c4af5ec2988c74b27ed1b79ec3891.png "boot")

新版本有一个 800×600 的液晶触摸屏。他们仍然使用开源的 Linux 后端，但是他们已经更新了用户界面。Chumby widgets 现在可以在设备上管理。以前，用户必须登录网站，然后将他们选择的小工具推送到 Chumby。该软件被设计成用户的主要照片管理应用程序。它可以立即识别插入的存储卡，并允许用户将照片拖放到 widget 播放列表中。该设备与 PhotoBucket 无缝集成，让您可以轻松上传新的图库。您也可以将这些发送给其他 Chumby 用户(Chums)。

![overview-2](img/0d89afc407186d7614241223d15e38e0.png "overview-2")

请记住，这只是一个评估套件，所以它安装在一个通用的木制相框中。

*![small_back](img/cdd12f5979eba4a3c8617e36f090eb5e.png "small_back")*

[*点击这里查看大图*](http://hackaday.com/wp-content/uploads/2009/01/big_back.jpg)

左侧是连接到板载放大器的立体声扬声器。底部的大橙色带包含所有的显示电子设备。右边较低的连接器为背光供电。上方的四线丝带用于触摸屏。顶部的切口是用于 USB [WiFi](http://www.mahalo.com/WiFi "WiFi - Mahalo") 卡的。硬币盒是实时时钟的备用电池。顶部有两个控制面板按钮。

![headers](img/f6ae7ef8e9ff358ea61c141a9bc811cd.png "headers")

该板包括几个接头，以便于调试。左下角的引脚提供了一个串行控制台([细节](http://hackaday.com/wp-content/uploads/2009/01/3210605127_ca9b1f9fae.jpg))。较大的分组是 CPU JTAG。接下来是用于初始引导映像的 MMC 端口。密码处理器也有一个 JTAG 连接器。

![camera](img/444d06b73a2c1cdab85d05de15b3b753.png "camera")

翻转电路板，您可以看到可选的摄像机子卡。

![stamp](img/e07c3e12d2d88a3eeac315e26d190c48.png "stamp")

正面 RAM 旁边的丝印上写着这个板版本是暴风 v8.0 revC。

*![small_front](img/1e9fbcd1db17c4c886973179cfe6a673.png "small_front")*

[*点击这里查看大图*](http://hackaday.com/wp-content/uploads/2009/01/big_front.jpg)

棋盘的正面是最有趣的部分。重置和用户按钮位于左上角。旁边是 SD 卡插座和 CF 卡插座。电源插孔和麦克风与放大器电路一起位于右上角。CF 下方是一个 TSOP 插座，用于容纳 Hynix HY27UF081G2A-TP 存储设备。在那下面是主处理器，一个[三星 S3C6410](http://www.samsung.com/global/business/semiconductor/productInfo.do?fmly_id=229&partnum=S3C6410) 。是 533Mhz 的 ARM11 CPU。芯片的右边是两个 Hynix RAM 芯片。这款新的 Chumby 可以构建 2-8GB 的存储空间。下面是 Novatek NT39703 显示驱动程序。密码处理器在那边。耳机插孔位于主板的右下角。主板的下边缘有三个 USB 端口。其中一个插了 USB WiFi 卡。我们假设不集成 WiFi 意味着他们不必处理 FCC 的批准；他们只使用认可的卡。 [USB](http://www.mahalo.com/USB "USB - Mahalo") 和存储卡由位于相机模块旁边的 Alcor Micro AU6350 控制。

对于那些想了解更多细节的人，这里有完整的原理图:

**重要提示:**本下载中包含的材料受下载中包含的[查比 HDK 许可协议](http://www.chumby.com/developers/agreement "chumby › chumby hdk license agreement")的约束。通过在此下载中使用 Chumby 材料，您表明您已经阅读并理解该协议，并同意受其约束。

[下载查比暴风城 HDK](http://blog.mahalo.com/hackaday/chumby/chumby.stormwind.hdk.zip)