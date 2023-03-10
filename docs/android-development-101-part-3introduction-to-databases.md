# Android 开发 101–第 3 部分:数据库介绍

> 原文：<https://hackaday.com/2010/07/21/android-development-101-part-3introduction-to-databases/>

在本教程中，我们将从上一篇关于[图形元素](http://hackaday.com/2010/07/19/android-development-101-part-2improved-hello-world/)的教程转向关注 Android 开发中的数据库。android 平台在其应用程序中使用 SQLite 数据库，并且是 android 开发中五个数据存储选项之一。我们将只关注 android 中的 SQLite 开发，因为它是构建一个可行/功能性程序的关键。学完本教程后，您应该能够实现一个 SQLite 数据库，然后能够从数据库的表中插入和选择项目。

对于这个项目，我们将创建一个随机报价生成器，让你在文本框中输入报价或谚语，然后按下按钮，将它们插入到数据库中。我们将发出一个确认消息，让我们看到数据是否成功地输入到数据库中，文本框将是空白的。如果按下第二个按钮，数据库将被访问，并被告知从数据库中选择一个随机报价，以显示在屏幕上的祝酒词中。

首先，我们将制作一个名为 **RandomQuotes** 的新项目。在[系列的第一部分](http://hackaday.com/2010/07/15/android-dev-101-%E2%80%93-part-1hello-world/)中，我们逐步完成了一个新项目，所以我们不会再重复所有的步骤，而是我会给你你需要的信息。启动并运行这个项目的信息如下:

*   **项目名称:**随机报价
*   **构建目标:** Android 1.5
*   **应用名称:**随机报价
*   **包名:** com.gregjacobs.randomquotes
*   **创建活动:**报价主
*   **最小 SDK 版本:** 3

[![](img/70bfca64a7547fb5d694a0ec5cf81669.png "Part3-Databases001")](http://hackaday.com/wp-content/uploads/2010/07/part3-databases001.png)

插入这些值并按下 Finish 后，我们将开始在我们的*com . Greg Jacobs . random quotes*包中创建一个类文件。为此，我们将右键单击该包并导航至**新**，然后导航至**类**。当新窗口弹出时，我们将输入的唯一数据是用 **DBAdapter** 填充的 **Name** 部分。完成后，我们按下 **Finish** 并显示一个简单的类文件，我们将很快开始修改它。本教程将像上一个一样，代码将被发布，我将解释重要的部分和功能是什么。与之前的教程代码的唯一区别是，我在这里包含了文本文件和代码文档，以便您能够下载和比较。我们将从*DBAdapter.java*文件开始:

[![](img/ff6c6eacd811f9d292928aca543905fa.png "Part3 - Final Product - 005")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-005.png)[![](img/81cc830b4b1dc46d46288db51c9580bf.png "Part3 - Final Product - 006")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-006.png)[![](img/9c00e8cfa3d9887bb102ae8d927dad22.png "Part3 - Final Product - 007")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-007.png)[![](img/093d926ce4172fc4df31191a1f613eea.png "Part3 - Final Product - 008")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-008.png)

```

package com.gregjacobs.randomquotes;

import java.util.Random;

import android.content.ContentValues;
import android.content.Context;
import android.database.Cursor;
import android.database.SQLException;
import android.database.sqlite.SQLiteDatabase;
import android.database.sqlite.SQLiteOpenHelper;
import android.util.Log;

```

我们将从导入启动和运行这个 SQLite 数据库所需的所有工具开始。所有这些对数据库程序员来说可能都很简单，但我们还是会讨论它们。 **ContentValues** 允许我们为 insert 语句存储一组值，**上下文**如上一篇文章中所解释的，允许我们访问应用程序环境。 **Cursor** 可能是除 SQLite 导入之外我们需要的最重要的导入。Cursor 允许我们访问从数据库查询返回到 cursor 的数据。SQLException 允许我们在出现错误时抛出 SQL 异常，这些消息提供了更多关于问题可能是什么的信息。 **SQLiteDatabase** 让我们能够使用方法管理 SQLite 数据库。SQLiteOpenHelper 基本上是一个助手类，允许创建和版本管理数据库。 **Log** 基本上会记录错误情况下的输出。

```

public class DBAdapter
{
    int id = 0;
    public static final String KEY_ROWID = &quot;_id&quot;;
    public static final String KEY_QUOTE = &quot;Quote&quot;;
    private static final String TAG = &quot;DBAdapter&quot;;

    private static final String DATABASE_NAME = &quot;Random&quot;;
    private static final String DATABASE_TABLE = &quot;tblRandomQuotes&quot;;
    private static final int DATABASE_VERSION = 1;

    private static final String DATABASE_CREATE =
        &quot;create table tblRandomQuotes (_id integer primary key autoincrement, &quot;
        + &quot;Quote text not null );&quot;;

    private final Context context;

    private DatabaseHelper DBHelper;
    private SQLiteDatabase db;

```

在这里，我们定义了要在数据库中使用的所有变量，从数据库名称一直到数据库 create 语句。我们使用 final 变量，因为它们永远不会改变值，为表名等创建一个变量会比硬编码我们所有的值和提交太多(记住可重用性)更容易。

```

    public DBAdapter(Context ctx)
    {
        this.context = ctx;
        DBHelper = new DatabaseHelper(context);
    }

	private static class DatabaseHelper extends SQLiteOpenHelper
    {
        DatabaseHelper(Context context)
        {
            super(context, DATABASE_NAME, null, DATABASE_VERSION);
        }

        @Override
        public void onCreate(SQLiteDatabase db)
        {
            db.execSQL(DATABASE_CREATE);
        }

        @Override
        public void onUpgrade(SQLiteDatabase db, int oldVersion,
                              int newVersion)
        {
            Log.w(TAG, &quot;Upgrading database from version &quot; + oldVersion
                  + &quot; to &quot;
                  + newVersion + &quot;, which will destroy all old data&quot;);
            db.execSQL(&quot;DROP TABLE IF EXISTS tblRandomQuotes&quot;);
            onCreate(db);
        }
    }

```

上面我们定义了一个构造函数来获取应用程序的上下文，并将其扩展到构造函数下的 DatabaseHelper。 **DatabaseHelper** 类扩展了我们的 **SQLiteOpenHelper** ，这将为我们的 SQLite 数据库管理添加更强大的功能。我们将在后面看到使用的关键函数是 **onCreate** ，它允许我们执行 SQL 语句来创建数据库。

```

    //---opens the database---
    public DBAdapter open() throws SQLException
    {
        db = DBHelper.getWritableDatabase();
        return this;
    }

    //---closes the database---
    public void close()
    {
        DBHelper.close();
    }

```

上面我们有两个关键函数，允许我们打开和关闭数据库，当在我们的主*中调用它们时可以引用它们。java* 文件。

```

    //---insert a title into the database---
    public long insertQuote(String Quote)
    {
        ContentValues initialValues = new ContentValues();
        initialValues.put(KEY_QUOTE, Quote);
        return db.insert(DATABASE_TABLE, null, initialValues);
    }

```

当我们在 main *中调用报价时，上面的函数将处理我们的报价。java* 文件。它还将通过将字符串**引用**放入名为 **initialValues** 的**内容值**中，然后将其插入到数据库表中，为它们进入数据库做好准备。

```

    public int getAllEntries()
    {
        Cursor cursor = db.rawQuery(
                    &quot;SELECT COUNT(Quote) FROM tblRandomQuotes&quot;, null);
                if(cursor.moveToFirst()) {
                    return cursor.getInt(0);
                }
                return cursor.getInt(0);

    }

```

该函数将查询数据库表中输入的报价数，这样它可以帮助随机数生成器选择多高的数字，这样我们就不会抛出异常。我们在很大程度上使用了 rawQuery，因为我个人不太喜欢 Android 处理查询的方式(让你分段输入语句的不同部分，并用逗号分隔),但我对它们允许你拥有原生 SQL 查询的全部功能印象深刻。if 语句将把光标移动到第一个结果(如果有很多结果的话)，并抓取它在那里看到的第一个整数。如果 If 语句不为真，它将从起始位置获取结果。

```

    public String getRandomEntry()
    {

    	id = getAllEntries();
    	Random random = new Random();
    	int rand = random.nextInt(getAllEntries());
    	if(rand == 0)
    		++rand;
        Cursor cursor = db.rawQuery(
                    &quot;SELECT Quote FROM tblRandomQuotes WHERE _id = &quot; + rand, null);
                if(cursor.moveToFirst()) {
                    return cursor.getString(0);
                }
                return cursor.getString(0);

    }

}

```

该函数将由主函数*调用。java* 程序根据数据库中的条目数返回一个随机结果。我们使用函数 **getAllEntries** 来获得报价的数量，然后我们告诉我们的随机变量，它不能高于 **id** 。在我们的 select 语句中，我们告诉它查找 quote **WHERE _id = rand** ，这是我们的随机数。

这个类文件完成后，我们就有了一个完全可重用的数据库适配器，可以开始向数据库中插入报价了。我们现在需要关注这两个 XML 文件，这将是一个快速的记忆之旅，所以代码和图片将被发布，我们不应该回顾，因为一切基本上都是从[最后一次发布](http://hackaday.com/2010/07/19/android-development-101-part-2improved-hello-world/)开始的。下面是 *main.xml* :

[![](img/b17e6fdb5dcec74a96704df2cb65ebc0.png "Part3 - Final Product - 010")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-010.png)

```

&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;LinearLayout xmlns:android=&quot;http://schemas.android.com/apk/res/android&quot;
    android:orientation=&quot;vertical&quot;
    android:layout_width=&quot;fill_parent&quot;
    android:layout_height=&quot;fill_parent&quot;
    &gt;
&lt;TextView
    android:layout_width=&quot;fill_parent&quot;
    android:layout_height=&quot;wrap_content&quot;
    android:text=&quot;@string/Quote&quot;
/&gt;
&lt;EditText
android:id=&quot;@+id/Quote&quot;
android:layout_width=&quot;fill_parent&quot;
android:layout_height=&quot;wrap_content&quot;
/&gt;
&lt;Button
android:id=&quot;@+id/go&quot;
android:layout_width=&quot;fill_parent&quot;
android:layout_height=&quot;wrap_content&quot;
android:text=&quot;@string/press&quot;
/&gt;
&lt;Button
android:id=&quot;@+id/genRan&quot;
android:layout_width=&quot;fill_parent&quot;
android:layout_height=&quot;wrap_content&quot;
android:text=&quot;@string/genRan&quot;
/&gt;
&lt;/LinearLayout&gt;

```

下面是 *strings.xml* 文件:

[![](img/b1c6c3a36dd032a048ef10767c18a1f8.png "Part3 - Final Product - 009")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-009.png)

```

&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;
&lt;resources&gt;
    &lt;string name=&quot;Quote&quot;&gt;Please Enter A Quote:&lt;/string&gt;
    &lt;string name=&quot;app_name&quot;&gt;Random Quotes&lt;/string&gt;
    &lt;string name=&quot;press&quot;&gt;Press Me!&lt;/string&gt;
    &lt;string name=&quot;genRan&quot;&gt;Generate Random Quote!&lt;/string&gt;
&lt;/resources&gt;

```

两者都非常简单，与这些文件和之前的帖子的唯一区别是在 *strings.xml* 中增加了一个字符串节点，在 *main.xml* 中增加了一个按钮。现在我们已经有了我们想要的布局，现在我们的任务是编写 QuotesMain.java*文件。这个文件将注册我们的两个按钮，并使用 switch 语句将它们连接到一个事件处理程序。下面是我们的*QuotesMain.java*文件的代码:*

[![](img/433c6d0369e933a3d8b75cb91772d16a.png "Part3 - Final Product - 011")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-011.png)[![](img/29f34e7b21c875436eb84b682bcde66a.png "Part3 - Final Product - 012")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-012.png)[![](img/ca730c6aa73796a151da404534f6a002.png "Part3 - Final Product - 013")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-013.png)

```

package com.gregjacobs.randomquotes;

import android.app.Activity;
import android.content.Context;
import android.os.Bundle;
import android.view.View;
import android.view.View.OnClickListener;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;

```

在这里，我们正在导入所有必需的项目，以便能够将这个项目整合在一起。从[图形元素](http://hackaday.com/2010/07/19/android-development-101-part-2improved-hello-world/)来看，所有这些你都应该很熟悉，如果还不熟悉，那么这是一篇很好的文章，你可以从这里开始着手。

```

public class QuotesMain extends Activity {
	DBAdapter db = new DBAdapter(this);
	EditText Quote;
    /** Called when the activity is first created. */
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.main);
        // Capture our button from layout
        Button setButton = (Button)findViewById(R.id.go);
        Button getButton = (Button)findViewById(R.id.genRan);
        // Register the onClick listener with the implementation above
        setButton.setOnClickListener(mAddListener);
        getButton.setOnClickListener(mAddListener);
    }

```

我们现在需要通过 id 引用按钮，它们是 **getButton** (从文本框中获取信息并将其插入数据库)和 **setButton** (根据数据库中的商品数量从数据库中检索随机报价)。这两个都有相同的事件处理程序，下面决定运行什么代码。

```

    // Create an anonymous implementation of OnClickListener
    private OnClickListener mAddListener = new OnClickListener()
    {
    	public void onClick(View v)
    	{
    		switch(v.getId())
    		{
    		case R.id.go:
				db.open();
				long id = 0;
				// do something when the button is clicked
				try
				{
					Quote = (EditText)findViewById(R.id.Quote);
					db.insertQuote(Quote.getText().toString());

					id = db.getAllEntries();

					Context context = getApplicationContext();
					CharSequence text = &quot;The quote '&quot; + Quote.getText() + &quot;' was added successfully!\nQuotes Total = &quot; + id;
					int duration = Toast.LENGTH_LONG;

					Toast toast = Toast.makeText(context, text, duration);
					toast.show();
					Quote.setText(&quot;&quot;);
				}
				catch (Exception ex)
				{
					Context context = getApplicationContext();
					CharSequence text = ex.toString() + &quot;ID = &quot; + id;
					int duration = Toast.LENGTH_LONG;

					Toast toast = Toast.makeText(context, text, duration);
					toast.show();
				}
				db.close();
				break;

```

在上面的 case 语句中，我们可以看到，我们从 textbox 中获取文本，并使用来自 **DBAdapter** java 类的 **db.insertQuote** 将数据插入数据库。成功插入后，我们将显示一个提示，让我们可以看到成功输入的报价以及数据库中的报价数量。

```

    		case R.id.genRan:
    			db.open();
    			//long id1 = 0;
    			// do something when the button is clicked
    			try
    			{
    				String quote = &quot;&quot;;
    				quote = db.getRandomEntry();
    				Context context = getApplicationContext();
    				CharSequence text = quote;
    				int duration = Toast.LENGTH_LONG;

    				Toast toast = Toast.makeText(context, text, duration);
    				toast.show();
    			}
    			catch (Exception ex)
    			{
    				Context context = getApplicationContext();
    				CharSequence text = ex.toString();
    				int duration = Toast.LENGTH_LONG;

    				Toast toast = Toast.makeText(context, text, duration);
    				toast.show();
    			}
    			db.close();
    		}
		}
    };
}

```

这个例子使用一个字符串变量来引用我们使用**db . getrandommentry**从数据库中取出的随机条目。然后，我们在一个 toast 中显示该数据，以表明该信息确实被获取了。所有这些代码放在一起并显示在 android 屏幕上时应该是这样的:

输入文本:

[![](img/94d7c02b1c03edfaa16877580e9fbaf6.png "Part3 - Final Product - 001")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-001.png)

显示随机条目:

[![](img/4a0bed6bd4e7b7bf5aaa0b47e723fce3.png "Part3 - Final Product - 002") ](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-002.png) [ ![](img/1629973f40714626bbb234c2f9dacb85.png "Part3 - Final Product - 003")](http://hackaday.com/wp-content/uploads/2010/07/part3-final-product-003.png)

介绍完 android 数据库后，你可以开始编写需要数据存储的应用程序，比如第一篇文章中提到的最终产品。在 android 的 SQLite 数据库中还有很多其他的特性。更多的内容将在下一个教程中介绍。诸如更新数据库、删除条目以及熟悉 DDMS(dal vik Debug Monitor Service)之类的事情都是 android 编程的重要组成部分。如果你不能等到下一篇文章来检查这些关于 [DDMS](http://developer.android.com/guide/developing/tools/ddms.html) 和[更新和删除](http://www.devx.com/wireless/Article/40842/1954)的文章。一如既往，如果任何人有问题，疑问或议题，不要犹豫地问，我会尽最大努力在下一个帖子之前回复你！直到下一次，快乐黑客！

用于比较的代码文本文件:

[db adapter](http://hackaday.com/wp-content/uploads/2010/07/dbadapter-java.doc)|[strings](http://hackaday.com/wp-content/uploads/2010/07/strings.doc)|[main](http://hackaday.com/wp-content/uploads/2010/07/main.doc)|[quote main](http://hackaday.com/wp-content/uploads/2010/07/quotesmain.doc)

用于参考的文章:

DevX—[在 Android 中创建和使用数据库](http://www.devx.com/wireless/Article/40842/1954)
Android 开发者—[参考指南](http://developer.android.com/guide/index.html)

继续第 4 部分:[高级数据库/GUI 代码& DDMS](http://hackaday.com/2010/08/02/android-development-101-part-4advanced-databasegui-code-and-ddms/)

43.002684-81.21499