# 如何使用 Greasemonkey 叠加图像

> 原文：<https://hackaday.com/2009/10/26/how-to-overlay-images-by-using-greasemonkey/>

今天我们来看看如何为 Firefox 的 [Greasemonkey 插件编写脚本。这个插件允许我们使用 JavaScript 来改变网页在浏览器上的显示方式。只有运行特定脚本的 Firefox 副本才能看到这些变化。例如，我们将编写一个脚本，通过叠加上面看到的图像，为 Hack a Day 上的每篇文章的横幅图像添加边框。休息之后看看是怎么做的。](https://addons.mozilla.org/en-US/firefox/addon/748)

**我们的目标:**

我们希望每篇文章的顶部图像看起来像是打印了白色边框，然后贴在页面的每个角落。这是一个我们曾经在我们的帖子上使用的效果，如果你错过了这个图像风格，Greasemonkey 脚本是一个重新实现这个效果的好方法。

**你需要什么:**

1.  安装[火狐](http://www.firefox.com)
2.  安装 [Greasemonkey 附件](https://addons.mozilla.org/en-US/firefox/addon/748)。
3.  下载并安装我们的脚本:[hack aday _ 怀旧. user.js](http://blog.mahalo.com/hackaday/misc/hackaday_nostalgia.user.js)

**工作原理:**

Greasemonkey 在 Firefox 已经加载的页面上运行 JavaScript。文件的第一部分是一组注释，告诉 Greasemonkey 它正在处理什么:

//= = user script = =
//@ name Hack aday 怀旧
//@ namespace【http://hackaday.com
//@ description 在 Hackaday 上覆盖文章图片的照片边框和胶带边角。
//@ include[http://hackaday.com/*](http://hackaday.com/*)
//= =/user script = =

名称、命名空间和包含行都是脚本运行所必需的。名字就是你想给你的脚本起的名字。名称空间是唯一标识脚本的 URL，以防有两个脚本同名。Include 告诉 Greasemonkey 这个脚本应该应用于哪些页面。在我们的例子中，我们只想对 hackaday.com 上的图像动手脚，所以我们已经包括了该域的所有地址。

既然我们已经确定了需要修改的页面，我们就可以解析文档并提取出需要修改的元素。首先要做的是检查我们目标的页面源:

```
<div class='snap_preview'><p><img class="alignnone size-full wp-image-17747" title="plotter-with-300w-laser" src="http://hackaday.com/wp-content/uploads/2009/10/plotter-with-300w-laser.jpg?w=470&h=313" alt="plotter-with-300w-laser" width="470" height="313" /></p>
```

稍微挖掘一下，我们就可以找到上面那行包含 IMG 元素的文章标题。我们很幸运，页面构建了包装在类“snap-preview”的 DIV 中的每个帖子。我们可以使用 Greasemonkey 来解析页面，寻找这些 div，然后修改每个 div 中的第一个 IMG 元素:

```
//get all DIVs of the snap_preview class
var allDivs, thisDiv;
allDivs = document.evaluate(
 "//div[@class='snap_preview']",
 document,
 null,
 XPathResult.UNORDERED_NODE_SNAPSHOT_TYPE,
 null);
```

在上面的代码中，我们使用 evaluate 函数来挑选出“快照预览”类中的 div。我们将它们加载到一个名为 allDivs 的数组中，然后我们可以遍历它:

```
//step through each DIV
for (var i=0; i<allDivs.snapshotLength; i++) {
 thisDiv = allDivs.snapshotItem(i);

 //Alter the first img of each DIV
 var image = thisDiv.getElementsByTagName('img');

 //Make sure we've got an IMG in this DIV
 if (image[0]) {

 //Save original source URL
 var orig_src = image[0].src;
 //Concatenate for CSS use
 orig_src = 'url(' + orig_src + ')';
 //Set original as background
 image[0].style.background = orig_src;

 //Set Hack a Day overlay as image
 image[0].src = 'http://hackaday.com/files/2009/10/had_frame.png';
 }
}
```

这段代码就是奇迹发生的地方。循环用于遍历我们在前面的代码片段中获取的每个 DIV。我们通过使用 getElementsByTagName 函数来获取 IMG 元素。所有 IMG 元素都被放入一个名为“image”的数组中，但是我们只想改变每篇文章中的第一张图片，所以我们总是引用 image[0]。

对于图像边框和胶带效果，我们使用 GIMP 创建一个 PNG 文件，它在我们希望原始图片显示的地方具有透明度。我们需要原始图片在覆盖图的后面，所以我们使用 CSS 属性“background”将它作为背景图片。然后，PNG 覆盖图被设置为 IMG 元素的新 SRC。

这就是所需要的，现在图片将被你在这篇文章顶部看到的边框图片覆盖。

**利弊:**

使用这个系统有一些缺点；叠加覆盖了原始图像的边界，已经有这种图像效果的旧帖子将再次应用它，叠加将被拉伸以匹配每个原始图像，这可能看起来很奇怪，取决于图像高度，并且我们提供的叠加图像质量相当低(你自己可能会做得更好)。

我们的方法使用了非常少量的代码，并且不需要重新计算原始图像的大小。

**下一步:**

现在，我们已经向您展示了如何做到这一点，您可能想要更进一步。原来的图片风格也是把图像做成黑白的。你能让脚本也这样做吗？为了朝着正确的方向开始，你可能想看看 [Pixastic JavaScript 图像操作库](http://www.pixastic.com/lib/)(网站死了，试试[互联网档案版本](https://web.archive.org/web/20091213134605/http://www.pixastic.com/lib/)和[GitHub repo](https://github.com/jseidelin/pixastic/))及其去饱和功能。

**不知所措？**

如果您需要一些帮助来解释我们在这里所做的事情，请使用您的在线资源:

*   [深入了解 Greasemonkey](http://diveintogreasemonkey.org/) :一本帮助你学习 Greasemonkey 脚本的在线书籍
*   HTML 狗:HTML 和 CSS 的最佳实践指南

[http://www.htmldog.com/](http://www.htmldog.com/)