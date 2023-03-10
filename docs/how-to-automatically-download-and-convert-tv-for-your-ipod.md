# 如何:为您的 IPod 自动下载和转换电视节目

> 原文：<https://hackaday.com/2005/10/19/how-to-automatically-download-and-convert-tv-for-your-ipod/>

Videora 的好人们最近在 T2 发布了 Videora iPod 转换器。使用这个工具，你可以让几乎任何视频 iPod 准备就绪。他们有一个方便的[方法来翻录和转码你自己的 DVD](http://www.videora.com/en-us/Converter/guides.html#1000)。我们的目标是使用 Bittorrent 自动下载电视，并将其转换为 iPod 友好的格式，为我们节省 2 美元。

首先你需要的是一个使用 Azureus 的功能广泛的系统。遵循我们的[广泛的操作指南](http://www.engadget.com/entry/1234000167021291/)来设置一个。BroadCatching 系统将自动下载您设置的电视节目。

在 Azureus 中需要配置两件重要的事情。转到"*工具- >选项*。勾选*保存到默认数据目录*旁边的复选框。选择下载文件时要保存文件的目录。勾选“*移动已完成的文件*”旁边的复选框。选择电视节目下载后要放置的目录。点击*保存*。Azureus 的配置已完成。

![Azureus config](img/31eebe4dc9f3cf107d751c0f3f3f6bb4.png)

要自动转换视频，你需要安装 [Videora](http://www.videora.com/en-us/Download/trial.html) 和 [Videora iPod 转换器](http://www.videora.com/en-us/Converter/iPod/download.php)。我们不会使用 Videora，但需要安装它才能打开 [xCasting](http://www.videora.com/en-us/Converter/xcast.html) 选项。

安装 Videora iPod 转换器后，在您准备开始之前，只需再做一些设置。点击*设置*。选取您想要放置 iPod ready 文件的目录。**更新:**h . 264 标准不能在 iPod 上使用。选择 SP 或 MPEG4。

![Videora config](img/6ad3ed9daf11a6a12ae65987b1847ba8.png)

对于 xCasting，您需要选择安装 Videora 的位置，然后才能配置它。选中“*自动排队*复选框，并选择存储已完成下载的目录。选择一个时间间隔来检查目录。点击*保存*。

![xCasting config](img/31730876b55362971d4779b94d2e7fb1.png)

现在，每当一个新文件出现在你的“完成”目录中，Videora 会自动将其添加到转换队列中。一旦文件被成功转换，它们将被放置在您的另一个文件夹中，准备传输到您的 iPod。转换器可以自动将文件复制到你的设备上，但我们无法测试这一功能，因为苹果仍然告诉我们它们是“处理订单”。祝你好运！