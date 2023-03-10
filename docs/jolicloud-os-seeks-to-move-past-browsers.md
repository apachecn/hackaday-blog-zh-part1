# Jolicloud 操作系统寻求超越浏览器

> 原文：<https://hackaday.com/2009/09/19/jolicloud-os-seeks-to-move-past-browsers/>

![jolicloud_apps](img/9f328b7a2c15cdb53056ffeb55da93df.png "jolicloud_apps")

Jolicloud 是一款针对上网本的新的基于 Linux 的操作系统。开发人员很友好，让我们接触到他们新操作系统的封闭开发版本。这个发行版是基于[Ubuntu Netbook Remix](http://www.ubuntu.com/GetUbuntu/download-netbook)(9.04 Jaunty Jackalope)构建的。乍一看，它只不过是换了新皮肤的 Ubuntu，但区别更深。Jolicloud 增加了一个应用商店类型的程序，提供网络应用程序和传统桌面应用程序的安装。使用 [Mozilla Prism](http://labs.mozilla.com/prism/) ，像脸书、Gmail 和维基百科这样的基于网络的应用被安装，在启动器中获得它们自己的图标，并且在没有浏览器的帮助下运行。

![jolicloud_wikipedia](img/dc81c0dc380ac4b2b819e13503e69304.png "jolicloud_wikipedia")

我们安装了维基百科并试了试。没有菜单和控件，只有顶部的标题栏和作为应用程序的网页。第一个问题是当点击进入一个页面，并意识到这不是我们想要的。通常情况下，后退按钮是我们的朋友，但 Prism 没有后退按钮。需要重新运行搜索以选择不同的结果。一个可取之处是，当点击外部链接时，会启动默认浏览器来处理新页面。

没有导航按钮不一定是一个交易破坏者。使用 Gmail 时，你多久按一次后退键？随着网络应用变得越来越像传统应用，我们认为界面都将趋向于自给自足，并使浏览器控件过时。

![jolicloud_social](img/8c58e6f9415c1c55073eb6036a8b2930.png "jolicloud_social")

除了应用程序安装，Jolicloud 应用程序还提供一些社交网络功能。每个用户都有自己的个人资料，并有以下，追随者和最新成员的列表。对我们来说，最有趣的功能是 Jolicloud 跟踪哪些计算机与您的帐户相关联。我们希望看到自定义和设置，如书签，随着我们从一台计算机到另一台计算机。

总之，我们对该产品的潜力感到非常兴奋。现在它是免费的，我们希望这项服务一旦发布就能保持下去。目前，我们对 Prism 的一瞥和笔记本功能的诱人进步感到满意。

### 想试用 Prism 却等不及 Jolicloud？

以下是如何不用等待 Jolicloud 的公开发布就能试用你的网络应用的方法。如果你运行的是 ubuntu，你可以在以下的软件仓库中找到它:

```
sudo apt-get install prism
```

如果你没有运行 Ubuntu，你可以从 Mozilla 下载 Prism。

通过键入“prism”从命令行运行。将弹出一个对话框:

![prism_dialog](img/d85e1cbef7bfe177da0ef74cae364afe.png "prism_dialog")

填写您的所有信息，这里我们运行 hackaday.com 作为一个应用程序。这将创建一个启动 web 应用程序的桌面快捷方式。

### 最后的想法

Jolicloud 从一个很棒的操作系统 Ubuntu Netbook Remix 开始，并以不同的方式使用现有的网络应用程序。我们认为开发人员在将 Prism 集成到他们的界面方面做得很好，并且发现它非常有用。只有时间能告诉我们用户是否愿意从传统的浏览方式转移到使用真正的网络应用:一个应用。