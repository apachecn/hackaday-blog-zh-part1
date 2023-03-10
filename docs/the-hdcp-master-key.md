# HDCP 万能钥匙

> 原文：<https://hackaday.com/2010/09/24/the-hdcp-master-key/>

![](img/f5cfd35e4afe0482faa9ddfcb406a44a.png "hdcp")

Pastebin 有[我们上周在帖子](http://pastebin.com/kqD56TmU)中谈到过[的 HDCP 万能钥匙](http://hackaday.com/2010/09/18/intel-high-bandwidth-digital-content-protection-cracked/)。这是一种加密协议，用于蓝光和高清有线电视等媒体上的 HDMI 内容保护。

主密钥数组是一组 40×40 的 56 位十六进制数组，用于生成密钥集。在文档的顶部有一个简短的段落，解释如何处理这些信息。如果你问我们，我们更感兴趣的是如何确定这一套。因此，为了获得一些背景信息，请阅读[键选择向量](http://en.wikipedia.org/wiki/Key_selection_vector) (KSV)维基百科页面。这将我们引向[一个有趣的讨论](http://cryptome.org/hdcp-weakness.htm)，提出如果可以捕获 40 个独特的特定于设备的 ksv，它们可以用来逆向工程主密钥。最后，一位 Reddit 用户(自己决定这些信息的可靠性)评论[拥有主密钥](http://www.reddit.com/r/technology/comments/ddj5f/hdcp_master_key_pirates_1_riaa_0/c0zfk0v)的价值。

在他的评论中，[iHelix150]涵盖了 HDCP 用来禁止被用来规避版权保护的设备的撤销系统。他说，有了主密钥，就有可能将你自己的撤销列表推送到设备上。每次列表写入您的设备(电视、蓝光等)时。)列表的版本号字段被更新。如果您在撤销列表中没有任何内容的情况下推送更新，并将版本号设置为全 1 的二进制值，将会阻止列表的任何重写。这意味着任何以前被禁止的硬件将被允许回到链或信任中。

到目前为止，这对你来说可能没有任何意义。但是看着这场猫捉老鼠的 DRM 之争很好玩不是吗？