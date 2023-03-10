# 夏普发展 101-系列教程

> 原文：<https://hackaday.com/2010/09/03/c-sharp-development-101-a-tutorial-series/>

![](img/7b1e28cb831abc8a8934749520f68c13.png "cdev")

In this tutorial series we are going to look at C# Development using the Visual Studio 2010 Express editions.  This will take you from the basics of installing Visual Studio 2010 Express, to the Object Oriented Programming style associated with C# and other languages, dabble in some database access (Access & SQL Server Express) and finally, design a project that will pull all of our knowledge together into a final solution.

我们将从微软的[网站](http://bit.ly/VS2010Express)下载 Visual Studio 2010 express 开始，这样我们就可以开始一些 C#开发了。文件下载完成后，您需要连接到互联网，以便程序可以下载必要的文件来完成安装。出于定制的考虑，我们不会完成安装的其余部分，我们会添加一些插件，让您的编码体验更加轻松。

现在已经安装了速成版，知道 Visual Studio 2010 速成版不支持扩展性是件好事。这意味着不包括安装插件和附加组件的能力。如果您碰巧获得或拥有 Visual Studio 2010 的完整版本，那么您可以选择添加这些插件，这些插件曾经帮助我摆脱了困境。

*   [视觉辅助 X](http://bit.ly/WholeTomato)
    *   这可能是智能感知和文档语法突出显示的最佳应用程序之一。现在你们中的许多人可能会说 Visual Studio 已经做到了这一点。是的，它们可以，但不如 Visual Assist X。这个附加组件将查看您添加的文件，如 Boost 库，并检索所有的 Boost 函数，并尝试拼凑特定函数将做什么的描述。语法高亮显示是最好的，快速选项可以从最小到最大高亮显示。对于狂热的程序员来说这是必须的，但是一年的订阅费是 249 美元，以后每年的维护费是 49 美元。这个价格标签可能会让大多数人望而却步，但不妨试用 30 天，试一试。

[![](img/7feb0454919a36e99056d59358d71f88.png "wtsLogoGray")](http://hackaday.com/wp-content/uploads/2010/09/wtslogogray.gif)

*   [幽灵 Doc](http://bit.ly/GhostDoc)
    *   作为 SubMain 的产品，这个附加组件将允许您使用 XML 标记快速有效地记录代码。为了生成这些注释，它使用元素类型、函数参数及其名称来生成注释。这对于不喜欢在代码中记录函数的人来说尤其有用。最有前途的附加软件，如果你正在寻找代码文档。

![](img/e22e0515c43a9991f19b4cb7b219d887.png)

*   [AnkhSVN](http://bit.ly/Ankh_SVN)
    *   一个免费的 Visual Studio SVN 加载项，允许您在舒适的 Visual Studio 环境中连接到存储库、浏览分支。对于想在 Google Code 上开始一个社区项目或主持他们自己的项目的人来说，非常容易使用。对于那些喜欢协作而不想停留在一个人的电脑上查看代码的人来说，这是必备的。

![AnkhSVN logo](img/667a5188c94fc9a79621701ee762d6d7.png)

All of these have been personally used and are highly recommended for use when developing for the .NET framework.  The next part in this series will go back to an old classic for programmers; Hello World.  We will go through making a project file and printing Hello World to the console as well as on a form.  As always, any problems with the series or if you just have questions post to the comments so that we may learn from each others mistakes and grow as a community.  If you can’t wait until the next post, [here](http://bit.ly/CSharpHelloWorld) is how to start making a Hello World console app.  Until next time, Happy Hacking!43.002684-81.21499