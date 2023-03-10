# Android 开发 101–第 6 部分:为市场做好准备！

> 原文：<https://hackaday.com/2010/08/10/android-development-101-part-6getting-ready-for-market/>

[![](img/c1f214ef804138670a8524e89fa5dc08.png "android-market-apps")](http://hackaday.com/wp-content/uploads/2010/08/android-market-apps.jpg)In this tutorial we are going to cover packaging one of our applications into an .apk file and getting it ready for the Android Market.  After we have completed this tutorial you should be able to use the tools provided in the AndroidSDK to sign your application, put the application on your phone and install it or send it to the Android Market.  These will be great assets to have if you decide to develop applications that you may want to charge for.  This tutorial will also be a change from the normal ones because it will include little, if any, code. To start off, if you have great aspirations for marketing your applications to others make sure to sign up for a [developer account](http://market.android.com/publish/Home) and pay the one time fee of **$25 USD**.  This will ensure that not just anyone is publishing to the market.  If your not looking to shell out the money then you can continue with the tutorial and give anyone who wants your app the file to put on their SD card. Whether you decide to do this step or not we still need to version our application.  We are going to use the **EnhancedQuotes** Project for this example.  We are going to open up the **Android Manifest** in enhanced quotes and put some code in here so we can version our application.

对应用程序进行版本控制意味着我们要让应用程序能够接受更新，如果某些东西坏了或者我们增加了更多的功能。一旦 Android 清单打开，我们将修改如下代码行

```

&lt;manifest xmlns:android=&quot;http://schemas.android.com/apk/res/android&quot; package=&quot;com.gregjacobs.enhancedquotes&quot; &gt;

```

并加入

```

&lt;android:versionCode=”1” android:versionName=”1.0” &gt;

```

这样这条线应该看起来像

```

&lt;manifest xmlns:android=&quot;http://schemas.android.com/apk/res/android&quot; package=&quot;com.gregjacobs.enhancedquotes&quot; android:versionCode=”1” android:versionName=”1.0”&gt;

```

这告诉我们运行应用程序的设备，这是第一个版本，任何更高的版本都将被升级。我们还需要添加一个 minSDKVersion，以便 Android Market 可以告诉哪些设备可以使用我们的应用程序。我们需要添加

```

&lt;uses-sdk android:minSdkVersion=&quot;3&quot; /&gt;

```

在下面将要显示的/application 节点下。我们还希望添加一个特定的图标，以便我们的应用程序在个人设备上从所有其他应用程序中脱颖而出。我选择了[这个图标](http://www.iconarchive.com/icons/mysitemyway/clean-3d/48/glossy-3d-blue-shield-icon.png)并把它保存到一个容易找到的地方，命名为 icon.png，然后拖到 res/中的 drawable 文件夹中。Eclipse 将询问您是否想要覆盖，只需说是。 

![](img/b660e2ceec723940b7358e3055ae1d09.png "Manifest")

We now need a private key that will allow us to sign applications by using this key in the signing process. It will have to be your, it will show its either for your work or personal development depending on how its created and have a period of time before it expires.  To make a private key we are going to use the keytool found in our **C:/Program Files/Java/jre6** folder.  Once inside the jre6 folder, hold **shift** and **right click** on the bin folder and choose the option that says **Open command window here**.  Once in the command promp we are going to run **keytool** with a bunch of commands that will assist us in making a private key. The command to be entered into the command window will be as follows:

**keytool-genkey-v-keystore C:/mykeygen . keystore******-别名 MyKey-keyalg RSA-keysize 2048-有效期 10000。****

 **现在我们已经输入了命令，我们可以逐步执行并确定这些变量对 keytool 的作用。

*   **-genkey—**开始制作密钥对。
*   **-v–**允许向创建密钥库的用户显示输出。
*   **-keystore–**在这个变量之后将包含我们将要创建的密钥库的位置和名称。
*   **-alias–**如果您愿意，可以为密钥库提供一个较短的名称或昵称。
*   **-keyalg–**这是使用的加密类型，可以是 RSA 或 DSA 编码。
*   **-keysize-**生成的每个密钥的大小。按照 Google 的说法，建议至少为 2048 位或更高。默认值为 1024 位。
*   **-有效期—**密钥有效的天数。这应该不低于 10000，但建议更高。

After pressing enter when done entering the command above you will be prompted to answer a series of questions so Google can validate this key.  The first question will be a password for the key and it will prompt you to re-enter it as well.  The password will not show up when pressing keys but it is working and it is key to remember this password because we will use this when packaging our app.  Next question will ask for your first and last name.  The thirst question asks for the unit you are in, I put development since we are programming for android.  Next is your organization, remembering if you aren’t programming for one just enter your name or whatever you wish.  Next is just the city you are located in.  Then state or province depending on your locale.  Enter the two digit country code that you are in, for example Canada would be CA and United States of America would be US.  It will then prompt us if this information is correct, if it is type n yes then press enter.  It will now prompt you for a password for mykey, press enter as we will use the same key as the keystore password.

[![](img/b084513250b522de79feb2d7663c55eb.png "KeyStore")](http://hackaday.com/wp-content/uploads/2010/08/keystore.png)

我们现在准备签署应用程序，并准备好部署到 Android 市场。我们通过进入 eclipse，在包浏览器中右键点击 EnhancedQuotes，进入 **Android Tools** ，然后点击**Export Signed Application Package…**。这将打开一个对话框，询问您想要导出的项目，单击**下一步**，选择我们想要的项目。现在，我们要单击该页面上的**浏览**按钮，找到我们之前创建的密钥库文件，确保输入其密码，然后单击**下一步**。选择我们为其创建的别名，并输入与之前相同的密码，然后单击下一步的**。现在为我们将要创建的 *APK* 文件选择目的地，我选择的是 **C 盘**。点击 Finish，APK 文件将会在我们选择的目录下被创建。**

[![](img/f438c1dfa78acd7a94f8c62408b9eb59.png "DevSite")](http://hackaday.com/wp-content/uploads/2010/08/devsite.png)[![](img/469da50268a9f2b292cadd9a45ab025d.png "DevSite1")](http://hackaday.com/wp-content/uploads/2010/08/devsite1.png)[![](img/14302d228789b70dc1781c2988870085.png "DevSite2")](http://hackaday.com/wp-content/uploads/2010/08/devsite2.png)[![](img/9eb75d0b117fca84255e6abbed669ced.png "DevSite3")](http://hackaday.com/wp-content/uploads/2010/08/devsite3.png)[![](img/d2799ae7a5e29b49a208b3d988ee7605.png "DevSite4")](http://hackaday.com/wp-content/uploads/2010/08/devsite4.png)
We now have two choices for publishing our app, the first being deploy on your android device by dropping it on the SD card and downloading an app installer like **appInstaller** from the marketplace or deploy to the android community via the **Developer Publish** site.  We are going to publish to market in this tutorial.  Navigate to the [publisher site](http://market.android.com/publish/Home), log in and then click on the button that says **Upload Application**.  We now need to find the *APK* file via the first browse button then enter some information about the application.  After filling out the *Title, Description, Application type and category, choosing your publishing options and filling out contact information and finally agree to the terms by checking the checkboxes* we can finally press **Publish**.  After pressing Publish the application is sent to the market and you can have millions of Android users use your application.  In the demo of this application the app I signed was actually sent to market and can be found by clicking search in the Market and entering in **Quotes Viewer/Generator**.  The link provided will only work on an android device, or you could scan the QR code below if you wanted to get there faster.

[![](img/111c402e0aff34b29fec39c3676d0120.png "Android Developer")](http://hackaday.com/wp-content/uploads/2010/08/android-developer.png)

[APK 文件](http://gregrjacobs.com/apps/Android/EnhancedQuotes.apk)

这一系列教程涵盖了在 Android 环境中开发应用程序的基础知识，包括打包应用程序并将其投入市场。现在我们已经有了 Android 开发的基础，我们可以开始关于更高级主题的教程，包括但不限于蓝牙控制/聊天。我希望每个读过 Android Development 101 的人都觉得它很有用，并期待更多。黑客快乐，直到下一个教程！

43.002684-81.21499**