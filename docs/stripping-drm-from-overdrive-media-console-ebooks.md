# 从 OverDrive 媒体控制台电子书中剥离 DRM

> 原文：<https://hackaday.com/2011/06/07/stripping-drm-from-overdrive-media-console-ebooks/>

![stripping_drm_from_overdrive_media_center_ebooks](img/443d1fefbe0306d6eed14249fce9895d.png "stripping_drm_from_overdrive_media_center_ebooks")

当地图书馆最近开始通过 OverDrive 媒体控制台系统借阅电子书。他借了几本书，这让他开始思考版权保护方案是如何实施的。他想知道，如果用户想在不同的或不受支持的硬件上查看他们已经借出的书，他们有什么办法。

他的研究围绕 Adobe 娴熟的数字版权管理方案展开，该方案用于保护 OverDrive 提供的图书。该主题分为三个部分，[首先介绍 EPUB 文件结构](http://www.geek-republic.com/2011/05/31/stripping-drm-overdrive-media-console-epubs-part-1/)，OverDrive 媒体控制台，以及前面提到的 ADEPT DRM 方案。

[第二部分仔细观察 OverDrive 媒体控制台本身](http://www.geek-republic.com/2011/06/01/stripping-drm-overdrive-media-console-epubs-part-2/)，在那里他使用由【I♥CABBAGES】编写的 ineptkey 和 ineptepub 实用程序从他发现的 epub 数据中提取 RSA 加密密钥。然而，当他试图从他的书中剥离 ADEPT DRM 层时，他发现 OverDrive 使用的是 ADEPT 标准的不兼容版本，这使得现有的工具变得无用。

[[阿明]讨论的最后部分更深入地挖掘了](http://www.geek-republic.com/2011/06/06/stripping-drm-overdrive-media-console-epubs-part-3/)OverDrive 控制台的内部工作原理，他发现 OverDrive 媒体控制台在 SQLite 数据库中存储了相当多的信息。经过一番挖掘，他找到了从他的书中剥离 DRM 所需的所有数据。[阿明]还花时间将他所有的发现打包成一个名为 OMCStrip 的小工具，正如你可能已经猜到的，它可以轻松地从 ADEPT 保护的电子书中剥离 DRM。