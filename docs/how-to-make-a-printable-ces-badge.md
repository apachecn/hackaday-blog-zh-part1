# 如何:制作可打印的 CES 徽章

> 原文：<https://hackaday.com/2010/01/12/how-to-make-a-printable-ces-badge/>

![](img/fa41eb05976517374df72b4fadb387eb.png "Large_Badge_in_Printer")

我们认为我们已经让你浏览了足够多关于我们的 CES 徽章的帖子，却没有告诉你我们是如何做到的或者如何得到一个徽章。本指南将介绍从 dxf 文件为徽标创建徽章的过程。然后我们会告诉你哪里可以买到。

首先，你需要一个 2D cad 程序，我们用的是 [QCad](http://www.qcad.org/) 。稍后你将需要 [OpenSCAD](http://openscad.org/) 。现在，拿起你选择的一个 dxf 标志。在这里，试试我们的[标志](http://www.thingiverse.com/download:4256) (R12 型 dxf)，这样你就可以跟着做了。在 QCad 中打开徽标 dxf 文件。

![](img/b0eb3be0730de539ca29b6396115cc80.png "QCad_open_dxf")

现在，您应该可以在 QCad 中看到您的徽标。这很好，很漂亮，但它不太适合 OpenSCAD。你需要为不同的部分准备不同的层。我们有一个头骨轮廓层，面部特征层，和一个扳手层。除了为单独的部分设置单独的层，我们还需要确保一行中没有三个样条点，因为 OpenSCAD 不能给你一个 stl。另外，在这种情况下，扳手甚至不会碰到头骨。是时候做一些样条了。

![](img/589f75cc5678143d17538b0d70c78308.png "QCad_edit_splines")

如果你现在发现下一部分太复杂，你可以跳过，但是当你在 OpenSCAD 中进入“编译和渲染”时，它显示你的对象不简单，你将不能导出一个 STL，因为你得到错误“对象不是一个单一的多面体或者无效！修改你的设计..”你必须回到这里来修复你的样条。关闭除了要修饰的图层之外的所有图层。创建一个新层来替换旧层。将新的命名为 new_foo，或者将旧的重命名为 old_foo。不管你怎么做，保持清晰，这样会容易得多。现在，突出显示旧层，你应该看到用于创建样条点。将捕捉设置为端点(捕捉->端点)，并开始绘制样条线(绘制->样条线->样条线)。注意窗口左下方的光标信息。如果一条线上有三个样条点，OpenSCAD 不会喜欢，所以您必须跳过三个点的中间来稍微改变您的样条。如何知道一条线上是否有三个样条点？嗯，对于网格绘制的样条曲线中最常见的情况，是当 x 或 y 坐标对于一行中的三个点不变时(即，具有点的样条曲线:{(1，1)，(2，1)，(5，1)}，y 坐标不变)。直线也可能有问题，但是没有太多的理由把很多直线做成直线。

![](img/696e1696194fe669d61f9c5aaeeb21c8.png "QCad_finished")

为清晰起见，标志的每个部分都有自己的颜色。将 dxf 的副本保存为 R12 dxf，OpenSCAD 更喜欢它。现在，让我们把它做成三维的。启动 OpenSCAD，并在您最喜欢的网络浏览器中打开 [OpenSCAD 用户手册](http://en.wikibooks.org/wiki/OpenSCAD_User_Manual)。下面是使整个工作正常的最终代码，复制并粘贴到 OpenSCAD 中:

```
logo_offset = [-104.281, -142, 0];
logo_scale = [0.65, 0.65, 1];

union()
{

	scale( v = logo_scale )
	{
		translate( logo_offset + [0, 0, -1])
		{

			dxf_linear_extrude(	file = "hack-a-day_logo-4-1.dxf",
						layer = "wrenches_a",
						height = 4,
						center = false,
						convexity = 10);
		}

		translate( logo_offset + [0, 0, -1])
		{
			dxf_linear_extrude(	file = "hack-a-day_logo-4-1.dxf",
						layer = "wrenches_b",
						height = 4,
						center = false,
						convexity = 10);

		}
	}

	intersection()
	{

		difference()
		{
			scale( v = logo_scale )
			{
				translate( logo_offset + [0, 0, -1] )
				{
					dxf_linear_extrude(	file = "hack-a-day_logo-4-1.dxf",
								layer = "skull",
								height = 25,
								center = false,
								convexity = 10);
				}
			}

			scale( v = logo_scale )
			{
				translate( logo_offset + [0, 0, 3] )
				{
					dxf_linear_extrude(	file = "hack-a-day_logo-4-1.dxf",
								layer = "face",
								height = 50,
								center = true,
								convexity = 10);
				}
			}		

			translate( v = [ 0, 0, 0 ] )
			{
				sphere( r = 15 );
			}	

		}
		translate( v = [ 0, 0, -10 ] )
		{
			sphere( r = 30 );
		}
	}
}
```

点击 F5 进行编译，您应该会在 OpenSCAD 的右上角看到 Hack a Day 徽标的渲染图。

logo_offset 和 logo_scale 变量将使 logo 居中并缩放。logo_offset 的值取决于徽标在 dxf 文件中的中心位置。

union()会将括号中的所有内容合并为一个内容。

您看到的 scale()将根据传递的向量，按一定的因子缩放括号内的内容。

translate()将括号内的内容移动一个由传递的向量决定的量。

dxf_linear_extrude()就像一个橡皮泥工厂，它根据传递的信息挤出一个形状:dxf 文件、图层和高度。center 变量确定挤出是以 z = 0 为中心(中心=真)还是从 z = 0 开始(中心=假)。凸度变量在低数值下看起来很难看。

交集()由括号内的两个相交的事物构成一个事物。

difference()取括号中的第一个东西，并从第一个东西中删除括号中的其余东西。

Sphere()生成一个传递半径的球体。

为了帮助您可视化此过程，请禁用所有 dxf_linear_extrude()和 sphere()行，方法是在它们前面加一个星号(' * ')。

删除前两个 dxf_linear_extrude()中的星号，并编译以使 OpenSCAD 联合、缩放、移动和挤出 dxf 的扳手层。这会产生一对交叉扳手:

![](img/24cfef2a4c3ca51208a7f09459355980.png "OpenSCAD_Wrenches")

让我们通过删除第三个 dxf_linear_extrude()行前面的星号来添加头骨轮廓，并编译:

![](img/4b3cf26c80b377095057eae9ff7fba9b.png "OpenSCAD_Add_Skull")

用井号(' # ')替换第四个 dxf_linear_extrude()行前面的星号，然后编译。这个英镑符号将以粉红色突出显示它前面的东西，帮助你看到它在哪里以及它在做什么，因为它正被从头骨中移除，所以你通常看不到它。

![](img/d4f496ee75c2d7bb89dd2dd2866989a2.png "OpenSCAD_Remove_Face")

去掉英镑符号，编译一下，你会看到眼睛和鼻子是如何通过把脸层的 dxf_linear_extrude()从头骨层的 dxf_linear_extrude()中去掉而形成的。

用英镑符号替换第一行的星号()并编译。

![](img/75014efcab6e11dc325ffbb3443ec8ca.png "OpenSCAD_Hollow_Skull-a")

根据你的观察角度，你可能看不到粉红色球体出现在头骨内。单击并按住图像，然后向上移动指针。现在，对象应该会随着指针旋转，直到您放开指针。旋转它可以看到头骨的背面。

![](img/268dd01befe5aae42b1b60714dd47c59.png "OpenSCAD_Hollow_Skull-b")

这应该有助于您看到第一个球体仍在差异()内，因此已从头骨挤出中移除。从第一行 sphere()中删除磅符号，然后编译。请注意，眼睛和鼻子挤出或球体()都没有从扳手上移除任何东西。这是因为扳手在差异之外()。它有助于保持中空，因为打印对象将使用更少的材料，您可以这样做:

![](img/66dcb107db18b61f652504a08780c2f9.png "IMG_0122")

如果不把头骨弄成空心的，把 LED 放入头骨会很困难。另外，大脑会去哪里？

现在这样的脸型是可以的，但是如果头骨有一个更圆的外观就更好了。删除最后一行的星号()并编译。

![](img/061212ad396a5b7c3503d9ac07189543.png "OpenSCAD_Finished")

头骨现在有一个圆形的脸。在交集()内，我们创建了创建具有平面和球体的头骨的差异()。你可以在它前面放一个英镑符号，然后编译，就可以看到球体了。交集()仅在两个部分都在的地方生成一个对象。您可以通过在 difference()和最后一个 sphere()线前面放置一个英镑符号来更好地了解这一点。

那么，你怎样才能得到这些东西呢？我们可以想出一些方法来得到一个，但是最好的两个方法是自己做一个或者为你做一个。

如果你有 3D 打印机，你可以自己制作。我们用了一个 MakerBot 纸杯蛋糕数控系统。制作自己徽章的文件在 [Thingiverse](http://www.thingiverse.com/thing:1562) 上。

如果你不知道或不想与拥有 3D 打印机的人交往，你可以通过 [Shapeways](http://shapeways.com/model/80960/large_hack_a_day_badge.html) 制作徽章。