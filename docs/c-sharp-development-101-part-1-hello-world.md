# 夏普发展 101-第一部分:你好世界

> 原文：<https://hackaday.com/2010/09/30/c-sharp-development-101-part-1-hello-world/>

![](img/fb8aa2df2ca4a31f1a019b8374d16607.png "cworld")

在本教程中，我们将近距离接触 Visual Studio 2010 环境。我们将学习如何制作一个控制台应用程序以及一个显示 hello world 应用程序的表单。这将使我们有机会查看 Visual Studio 中众多可用解决方案中的两种类型。我们将首先开始制作控制台应用程序，然后继续制作表单应用程序。

首先，我们必须了解我们将要使用的开发环境。最左侧是工具箱面板。这个面板让我们可以访问 Windows 窗体可以使用的许多控件。接下来是解决方案资源管理器，它将允许我们导航我们将在该解决方案中创建的项目和文件。“属性”面板直接位于我的解决方案资源管理器下，它允许我们更改控件的属性，以及我们稍后将创建的表单的属性。如果其中任何一项没有显示，可以从其他窗口下顶部的视图菜单中检索。有关 Visual Studio IDE 的更多信息，请访问 [MSDN](http://bit.ly/VSIDEHelp) 并搜索您遇到的具体问题。

[![](img/99d7cd4205f479cbe90a5615c4584cec.png "VisualStudioIDE")](http://hackaday.com/wp-content/uploads/2010/09/visualstudioide.png)

然后，我们需要启动 Visual Studio 环境并创建一个新项目。为此，我们将转到文件，然后导航到新项目并单击它。将出现一个对话框，询问您希望在解决方案中包含哪个将为您的项目自动创建的项目。我们需要使用控制台应用程序。接下来，我们需要将底部显示 **ConsoleApplication1** 的框替换为 **HelloWorldConsole** ，然后在创建项目和解决方案后，按 *CTRL-S* 将解决方案文件的名称更改为项目名称框下的框中的 **HelloWorld** ，并按 **OK** 。这将在解决方案文件中创建一个项目。解决方案文件就像是将解决方案文件中包含的所有项目绑定在一起的粘合剂。稍后，我们将发现这对于创建项目和创建引用我们将要编码的 DLL 的类文件是如何有益的。

创建项目后，我们将编辑 program.cs 文件。打开 program.cs 后，我们将添加必要的文本，使程序在控制台上输出“Hello World”。为此，我们将需要添加线**控制台。Out.WriteLine("Hello World！");**静态空主花括号内。完成后，我们现在可以构建并尝试构建我们的解决方案。为了构建解决方案，我们需要按下 *CTRL + SHIFT + B* ，构建过程将会是。构建成功后，我们现在可以通过按下 *CTRL + F5 来运行控制台应用程序。*这将显示一个命令提示符“Hello World！”。

[![](img/3ccba42501f338d320c0f4aa467827b8.png "HelloWorldConsole")](http://hackaday.com/wp-content/uploads/2010/09/helloworldconsole.png)

下面是 *program.cs:* 的源代码

```

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
namespace HelloWorldConsole
{
class Program
{
static void Main(string[] args)
{
Console.Out.WriteLine(&quot;Hello World!&quot;);
}
}
}

```

我们现在可以转到 Hello World 的 windows 窗体应用程序。要做到这一点，我们需要去解决方案和**右击**，然后去**添加**，然后点击**新项目**。对于这个项目，我们将其命名为 **HelloWorldForms** 。创建项目后，我们将删除 *Form1.cs* ，我们将通过右键单击 HelloWorldForms 项目，导航到 **Add** 然后到 **New Item** 来创建一个新表单，当对话框出现时，我们将选择 **Windows Form** 。

我们将使用的名称是 *main.cs* 并按下**添加**。我们现在编辑 *program.cs* ，将文件中可以找到的 **Form1** 改为 **main** 。创建 Windows 窗体后，我们可以开始从工具箱添加控件。
我们将把一个标签和一个按钮拖到程序中间的表单上。我们将在这里编辑属性，使标签内的文本为空白，标签的名称为 **lbHelloWorld** 而不是 **label1** 。完成后，我们将需要编辑之前放在表单上的按钮。我们将把按钮的名称改为 **btnHelloWorld** ，按钮的文本改为 **Click Me！**。完成后，我们将使用一个事件处理程序将按钮和标签绑定在一起，这样当按钮被点击时“Hello World！”会出现在标签中。

要为该按钮创建一个事件处理程序，我们将转到属性面板，并单击顶部看起来像闪电的按钮。这将把我们带到这个按钮可以处理的所有事件处理程序。我们需要 click 事件处理程序，这将创建处理 *main.cs* 中的 Click 事件所需的代码。现在包装器已经存在，我们可以在单击按钮时将输出编码到标签中。在 *main.cs* 中的“**private void btnHelloWorld _ Click**的花括号内，输入下面一行代码来链接这两个控件:

```

lbHelloWorld.Text = “Hello World!”;

```

这将使 *main.cs* 看起来像这样:

```

using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace HelloWorldForms
{
 public partial class main : Form
 {
 public main()
 {
 InitializeComponent();
 }

 private void btnHelloWorld_Click(object sender, EventArgs e)
 {
 lbHelloWorld.Text = &quot;Hello World!&quot;;
 }
 }
}

```

*program.cs* 应该是这样的:

```

using System;
using System.Collections.Generic;
using System.Linq;
using System.Windows.Forms;

namespace HelloWorldForms
{
 static class Program
 {
 /// &lt;summary&gt;
 /// The main entry point for the application.
 /// &lt;/summary&gt;
 [STAThread]
 static void Main()
 {
 Application.EnableVisualStyles();
 Application.SetCompatibleTextRenderingDefault(false);
 Application.Run(new main());
 }
 }
}

```

所有这些完成后，我们需要再次按下 *CTRL + F5* 来运行程序。应该出现的屏幕应该是这样的:

[![](img/f852e1d949f869b8899b2ef6cd67c8da.png "HelloWorldFormUnclicked")](http://hackaday.com/wp-content/uploads/2010/09/helloworldformunclicked.png)

按下按钮后的屏幕应该是这样的:

[![](img/0f42f4dbbd64edf3beaa7b037a04040a.png "HelloWorldFormclicked")](http://hackaday.com/wp-content/uploads/2010/09/helloworldformclicked.png)

现在我们已经完成了下一个教程，您应该能够在 Visual Studio IDE 中创建一个解决方案下的多个项目，删除项目中的文件并创建新的窗体和类，以及修改事件处理程序中的源代码。下一篇教程将更深入地介绍 Visual Studio 工具箱，用最少的主干代码制作一个带有控件的窗体，并回顾一些创建的常用文件以及自动包含的内容。关于工具箱控件的更多信息，你可以查看微软 MSDN 关于工具箱控件的文章。如果你在这个项目上有任何问题，请随时评论，我会帮助尝试和解决这个问题。直到下一个教程，快乐黑客！

43.002684-81.21499