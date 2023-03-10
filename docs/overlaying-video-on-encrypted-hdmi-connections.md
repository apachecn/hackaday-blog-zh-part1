# 在加密的 HDMI 连接上叠加视频

> 原文：<https://hackaday.com/2012/01/21/overlaying-video-on-encrypted-hdmi-connections/>

[邦尼]又在玩他的老把戏了。他成功地对 HDCP 安全的连接实施了[中间人攻击，以在任何 HDMI 视频流中覆盖视频。还有一个好处:~~他的黑客没有使用~~](http://www.bunniestudios.com/blog/?p=2117) [HDCP 万能钥匙](http://hackaday.com/2010/09/24/the-hdcp-master-key/)。它根本没有违反 DMCA。

HDCP 是一种可怕的加密方案，适用于兼容 HDMI 的设备。在 HDCP 之前，注入视频叠加甚至色度键控是合理使用的有效解释。[bunnie]认为 HDMI 设备应该具有与模拟设备相同的限制，所以他决定将自己的视频传输到电视上。

构建使用了 [NeTV](https://www.adafruit.com/products/609) ，这是一种方便而廉价的 FPGA 板，具有 HDMI 输入和输出。[bunnie]让 FPGA 窥探 HDMI 总线，并决定是否需要更改像素。这与几个月前德国的[研究人员所做的](http://hackaday.com/2011/11/30/hdcp-falls-to-fpga-based-man-in-the-middle-attack/)没有太大区别，但与学术安全研究人员不同的是，【邦尼】会给你一份购物清单，上面列着要买的东西。

作为他工作的一个例子，[bunnie]在 HDCP 加密的视频上实现了一个类似“tweet ticker”的东西。从色度键控、滤镜或简单地将 HDMI 流转储到硬盘，NeTV 设置几乎无所不能。查看[邦尼]演讲中的幻灯片，更好地了解他的所作所为。

[PAPPP]找到了一段视频。休息之后请继续关注。

[https://www.youtube.com/embed/37SBMyGoCAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent](https://www.youtube.com/embed/37SBMyGoCAU?version=3&rel=1&showsearch=0&showinfo=1&iv_load_policy=1&fs=1&hl=en-US&autohide=2&wmode=transparent)