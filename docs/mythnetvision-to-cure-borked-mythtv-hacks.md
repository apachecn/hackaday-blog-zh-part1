# 治疗流言电视黑客的流言电视

> 原文：<https://hackaday.com/2010/01/13/mythnetvision-to-cure-borked-mythtv-hacks/>

![](img/54bacd4630454d121e17b5e236a2bf36.png "mythnetvision")

另一组开发人员已经开始尝试将在线流媒体视频与 MythTV 整合。新插件名为 MythNetVision ，旨在方便合法地提供流媒体和下载视频功能。这意味着不违反提供网站的服务条款。

我们已经看到太多失败的尝试，很容易怀疑这个插件实际工作的可能性。像 [MythStream](http://home.kabelfoon.nl/~moongies/streamtuned.html) 和 [MythVodka](http://www.mythtv.org/wiki/MythVodka) 这样的插件在崩溃前只能暂时工作，而且似乎永远不会提供一个可靠的选项。许多人试图通过 MythTV UI 来添加 Boxee、[、Hulu Desktop](http://www.mythtv.org/wiki/Hulu_Desktop_Integration) 或 XBMC 集成，但这远不是一个干净的解决方案。

看起来，MythNetVision 采取了一种略有不同的方法。尽管还不可用，设计者已经分两部分构建了插件。前端是一个完全可皮肤化的用户界面，它解析 RSS 提要以提供浏览、搜索和查看视频所需的钩子。根据内容，可能会产生一个浏览器来播放视频，它可能会在 MythTV 的普通播放器中播放，或者在达到适当的缓冲水平后，可以启动一个单独的下载线程来播放视频。RSS 提要要么直接来自提供商，比如[的第三版提要](http://revision3.com/bestof/feed/Xvid-Small)，要么可以编写一个 scraper 从没有 RSS 提要的网站提供定制的 RSS 提要。

我们已经看到了进度的一瞥，我们乐观地认为我们会看到一个可靠的插件。早期采用和用户脚本贡献是帮助确保这一点的最佳方式，因此请密切关注该包的公开发布。