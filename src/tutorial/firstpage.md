在 web 服务器根目录（`DOCUMENT_ROOT`）下建立一个文件名为
`hello.php`，然后完成如下内容：

**示例 \#1 第一个 PHP 脚本：`hello.php`**

``` php
<html>
 <head>
  <title>PHP 测试</title>
 </head>
 <body>
 <?php echo '<p>Hello World</p>'; ?>
 </body>
</html>
```

在浏览器的地址栏里输入 web 服务器的 URL
访问这个文件，在结尾加上“/hello.php”。如果本地开发，那么这个 URL 一般是
*http://localhost/hello.php* 或者
*http://127.0.0.1/hello.php*，当然这取决于 web
服务器的设置。如果所有的设置都正确，那么这个文件将被 PHP
解析，浏览器中将会输出如下结果：

    <html>
     <head>
      <title>PHP 测试</title>
     </head>
     <body>
     <p>Hello World</p>
     </body>
    </html>

该程序非常的简单，它仅仅只是利用了 PHP 的 <span
class="function">echo</span> 语句显示了 *Hello
World*。用户一定不会满足与此。请注意该文件*无需被执行*或以任何方式指定。服务器会找到该文件并提供给
PHP
进行解释，因为使用了“.php”的扩展名，服务器已被配置成自动传递有着“.php”扩展名的文件给
PHP。一个普通的 HTML
文件，加上了几个特别的标签，就可以做很多非常有趣的事情！

如果试过了这个例子，但是没有得到任何输出，或者浏览器弹出了下载框，或者浏览器以文本方式显示了源文件，可能的原因是服务器还没有支持
PHP，或者没有正确配置。需要请服务器的管理员根据本手册“<a href="/install.html" class="link">安装</a>”一章的内容使得服务器支持
PHP。如果本地开发，请阅读手册有关安装的章节以确保所有的设置都正确。还要确认通过浏览器访问的
URL
确实指向了服务器上的这个文件。如果只是从本地文件系统调用这个文件，它不会被
PHP 解析。如果问题仍然存在，请通过
<a href="https://www.php.net/support.php" class="link external">» PHP 在线支持</a>中的各种方式获取帮助。

以上例子的目的是为了显示 PHP 特殊标识符的格式。在这个例子中，用 *\<?php*
来表示 PHP 标识符的起始，然后放入 PHP 语句并通过加上一个终止标识符 *?\>*
来退出 PHP 模式。可以根据自己的需要在 HTML 文件中像这样开启或关闭 PHP
模式。请参阅手册中“<a href="/language/basic-syntax.html" class="link">PHP 基本语法</a>”以获取更多信息。

> **Note**: <span class="info">**关于换行**  
> </span>
>
> 尽管换行在 HTML 中的实际意义不是很大，但适当地使用换行可以使 HTML
> 代码易读且美观。PHP 会在输出时自动删除其结束符 *?\>*
> 后的一个换行。该功能主要是针对在一个页面中嵌入多段 PHP
> 代码或者包含了无实质性输出的 PHP
> 文件而设计，与此同时也造成了一些疑惑。如果需要在 PHP 结束符 *?\>*
> 之后输出换行的话，可以在其后加一个空格，或者在最后的一个 echo/print
> 语句中加入一个换行。

> **Note**: <span class="info">**关于文本编辑器**  
> </span>
>
> 有很多文本编辑器以及集成开发环境（IDE）可以被用来建立、编辑和管理 PHP
> 文件。这些工具中的一部分被列在
> <a href="http://en.wikipedia.org/wiki/List_of_PHP_editors" class="link external">» PHP 编辑器列表</a>中。如果希望推荐其它的编辑器，请访问以上页面，并要求该页面的维护者将你推荐的编辑器加入到该列表中。使用支持语法高亮功能的编辑器会给开发带来很多帮助。

> **Note**: <span class="info">**关于文字处理器**  
> </span>
>
> 诸如 StarOffice Writer、Microsoft Word 和 Abiword
> 的文字处理器不适合用来编辑 PHP
> 程序。如果希望用以上这些工具的某一种来处理脚本，必须保证将结果存成了*纯文本*格式，否则
> PHP 将无法读取并运行这些脚本。

> **Note**: <span class="info">**关于 Windows 记事本**  
> </span>
>
> 如果使用 Windows 记事本来编写 PHP
> 脚本，需要注意在保存文件时，文件的后缀名应该为
> .php（记事本将自动在文件名后面加上 .txt
> 后缀，除非采取以下措施之一来避免这种情况）。当保存文件时，系统会让你指定文件的文件名，这时请将文件名加上引号（例如
> `"hello.php"`）。或者，也可以点击“另存为”对话框中的“保存类型”下拉菜单，并将设置改为“所有文件”。这样在输入文件名的时候就不用加引号了。

现在已经成功建立了一个简单的 PHP 脚本，那么再来建立一个最著名的 PHP
脚本！调用函数 <span
class="function">phpinfo</span>，将会看到很多有关自己系统的有用信息，例如<a href="/language/variables/predefined.html" class="link">预定义变量</a>、已经加载的
PHP
模块和<a href="/configuration.html" class="link">配置</a>信息。请花一些时间来查看这些重要的信息。

**示例 \#2 从 PHP 获取系统信息**

``` php
<?php phpinfo(); ?>
```
