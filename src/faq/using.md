使用 PHP
========

本节汇集了你在写 PHP 脚本时可能碰到的大多数普通错误。

1.  [我忘了 PHP
    函数的参数顺序，它们是随机的吗？](#faq.using.parameterorder)
2.  [我想写一个可以处理任何表单来的数据的通用 PHP 脚本。我怎么知道哪个
    POST 方法变量可用呢？](#faq.using.anyform)
3.  [我需要在所有的单引号（'）前加一个反斜线（\\），使它们变成（\\'）。我如何能够通过正则表达式来实现？
    我同样希望能够将 " 转换成 \\"，将 \\ 转换成
    \\\\。](#faq.using.addslashes)
4.  [我所有的 " 和 ' 都变成了 \\" 和
    \\'，我如何才能去掉这些不必要的反斜线？它们为什么及如何出现？](#faq.using.stripslashes)
5.  [PHP 选项 register\_globals 对我有什么影响？](#faq.register-globals)
6.  [当我这样做时，输出显示的次序是错的： \<?php function
    myfunc($argument) { echo $argument + 10; } $variable = 10; echo
    "myfunc($variable) = " . myfunc($variable); ?\>
    这是怎么回事？](#faq.using.wrong-order)
7.  [下面代码怎么没有分成两行显示？ \<pre\> \<?php echo "This should be
    the first line."; ?\> \<?php echo "This should show up after the new
    line above."; ?\> \</pre\>](#faq.using.newlines)
8.  [我得到消息 “Warning: Cannot send session cookie - headers already
    sent...” 或者 “Cannot add header information - headers already
    sent...”。](#faq.using.headers-sent)
9.  [我需要直接访问请求报头中的信息，怎么能办到？](#faq.using.header)
10. [当我用 IIS 进行 HTTP 认证时得到 “No Input file specified”
    消息。](#faq.using.authentication)
11. [Windows：不能访问另一台电脑上用 IIS
    共享的文件。](#faq.using.iis.sharing)
12. [我怎样混合使用 XML 和 PHP？它不认我的 \<?xml
    标记！](#faq.using.mixml)
13. [哪里可以找到所有可用的 PHP
    预定义变量的完整列表？](#faq.using.variables)
14. [怎样才能不用非免费的商业库（例如 PDFLib） 来生成 PDF
    文档？我想要个免费的并且不需要再连接别的 PDF
    库。](#faq.using.freepdf)
15. [我试着在用户自定义函数中访问一个标准的 CGI 变量（例如
    $DOCUMENT\_ROOT 或
    $HTTP\_REFERER），但是找不到，哪里出了错？](#faq.using.cgi-vars)
16. [有些 PHP 选项可以接受缩写的字节值，与仅能接受 integer
    字节值相反。都有哪些缩写字节值？](#faq.using.shorthandbytes)
17. [在 Windows 下，使用 localhost 访问的时候提示连接超时，但是使用
    "127.0.0.1" 的时候正常，为什么？](#faq.using.windowslocalhostissue)

**我忘了 PHP 函数的参数顺序，它们是随机的吗？**  
PHP
是一个将数百个外部库连接在一起的粘合剂，尽管有时候会有一些混乱。这里有一些简单的经验法则：

<a href="/book/array.html" class="link">数组函数</a> 参数的顺序为
"*needle, haystack*"，
<a href="/book/strings.html" class="link">字符串函数</a> 则相反，顺序为
"*haystack, needle*"。

<!-- -->

**我想写一个可以处理任何表单来的数据的通用 PHP 脚本。我怎么知道哪个 POST 方法变量可用呢？**  
PHP 提供很多“
<a href="/language/variables/predefined.html" class="link">预定义变量</a>”，例如超全局变量
`$_POST`。可以遍历 `$_POST`变量，因为它是一个和所有通过 POST
方法传递数据相联系的数组。例如，可以用
<a href="/control-structures/foreach.html" class="link">foreach</a>简单地遍历它，检查
<span class="function">empty</span>值，以及将它们输出。

``` php
<?php
$empty = $post = array();
foreach ($_POST as $varname => $varvalue) {
    if (empty($varvalue)) {
        $empty[$varname] = $varvalue;
    } else {
        $post[$varname] = $varvalue;
    }
}

print "<pre>";
if (empty($empty)) {
    print "None of the POSTed values are empty, posted:\n";
    var_dump($post);
} else {
    print "We have " . count($empty) . " empty values\n";
    print "Posted:\n"; var_dump($post);
    print "Empty:\n";  var_dump($empty);
    exit;
}
?>
```

<!-- -->

**我需要在所有的单引号（'）前加一个反斜线（\\），使它们变成（\\'）。我如何能够通过正则表达式来实现？ 我同样希望能够将 " 转换成 \\"，将 \\ 转换成 \\\\。**  
假设是针对数据库，请使用数据库自带的转义机制。比如，针对 MySQL 使用
<span class="function">mysql\_real\_escape\_string</span> 函数，针对
PostgreSQL 则使用 <span class="function">pg\_escape\_string</span>
函数。还有两个标准函数 <span class="function">addslashes</span> 和 <span
class="function">stripslashes</span> 可以在旧的 PHP
版本中实现类似的操作。

> **Note**: **设置选项说明： magic\_quotes\_gpc**  
>
> 设置选项<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>默认值为
> *on*。相当于对所有 GET, POST, and COOKIE 数据使用了 <span
> class="function">addslashes</span>。可以用 <span
> class="function">stripslashes</span> 来去掉它们。

<!-- -->

**我所有的 " 和 ' 都变成了 \\" 和 \\'，我如何才能去掉这些不必要的反斜线？它们为什么及如何出现？**  
最可能的情况是，由于 PHP 的
<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
被开启，反斜线神奇的存在了。这是 PHP
的一个旧特性引起的，应该被禁用，不要依赖它。另外， <span
class="function">stripslashes</span> 函数能够从 <span
class="type">string</span>中去掉所有的反斜线。

> **Note**: **设置选项说明： magic\_quotes\_gpc**  
>
> 设置选项<a href="/info/setup.html#" class="link">magic_quotes_gpc</a>默认值为
> *on*。相当于对所有 GET, POST, and COOKIE 数据使用了 <span
> class="function">addslashes</span>。可以用 <span
> class="function">stripslashes</span> 来去掉它们。

<!-- -->

**PHP 选项 register\_globals 对我有什么影响？**  
**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

首先要理解这个设置选项的作用。假如我们使用以下 URL：
*http://example.com/foo.php?animal=cat*，那么在
`foo.php`中我们可能会使用以下代码：

``` php
<?php
// 建议使用这种访问变量的方式
echo $_GET['animal'];

// 如果想直接访问 $animal 变量，就要把 register_globals 选项设置为 on
// 强烈建议不要这么做！！
echo $animal;

// 这个选项的值会影响到所有变量，包括 $_SERVER
echo $_SERVER['PHP_SELF'];

// 同样，要使 $PHP_SELF 变量自动生效，register_globals 选项必须设置为 on
// 强烈建议不要这么做！！
echo $PHP_SELF;
?>
```

上面的代码解释了 register\_globals
的作用，就是自动生成变量。多年来，这种编程方式被很多人所不喜，所以从 PHP
6 开始，这个选项就被禁用了。目前市面上绝大部分虚拟主机服务商也都默认把
register\_globals
禁用，但是请注意，你在阅读一些过时的资料时，可能仍有一些文章、教程、书籍要求把该选项开启。不用管它！

请参阅以下资源进一步了解：

-   <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
    选项说明
-   <a href="/security/globals.html" class="link">注册全局变量的安全问题</a>
-   <a href="/language/variables/external.html" class="link">处理外部变量</a>
-   使用
    <a href="/language/variables/superglobals.html" class="link">超级全局变量</a>
    的替代方案

> **Note**:
>
> 以上示例中，我们使用了一个 URL，其中包含了一个 QUERY\_STRING。PHP 会把
> QUERY\_STRING 中的信息通过 GET HTTP
> 请求传递，所以我们可以通过超级全局变量（superglobal） `$_GET`
> 来访问其中的变量。

**当我这样做时，输出显示的次序是错的：**

``` php
<?php
function myfunc($argument)
{
    echo $argument + 10;
}
$variable = 10;
echo "myfunc($variable) = " . myfunc($variable);
?>
```

这是怎么回事？

要在一个表达式中（例如在上面的例子中和其它字符串连接）使用函数的结果，需要
<span class="function">return</span> 这个值，而不是 <span
class="function">echo</span> 它。

**下面代码怎么没有分成两行显示？**

``` php
<pre>
<?php echo "This should be the first line."; ?>
<?php echo "This should show up after the new line above."; ?>
</pre>
```

在 PHP 中，一段代码的结束标记要么是“?\>”要么是“?\>\\n”（\\n
表示换行）。因此在上面的例子中，输出的句子将显示在同一行中，因为 PHP
忽略了代码结束标记后面的换行。这意味着如果要输出一个换行符，需要在每段
PHP 代码的结束标记后面多加一个换行。

PHP 为什么这么做呢？因为在格式化正常的 HTML
时，这样通常会更容易。假如输出了换行而你不需要这个换行时，就不得不用一个非常长的行来达到这样的效果，或者让产生的
HTML 页面的源文件的格式很难读。

**我得到消息 “Warning: Cannot send session cookie - headers already sent...” 或者 “Cannot add header information - headers already sent...”。**  
函数 <span class="function">header</span>， <span
class="function">setcookie</span> 和
<a href="/ref/session.html" class="link">session 函数</a>需要在输出流中添加头信息。但是头信息只能在其它任何输出内容之前发送。在使用这些函数前不能有任何（如
HTML）的输出。函数 <span class="function">headers\_sent</span>
能够检查脚本是否已经发送了头信息。请参阅
<a href="/ref/outcontrol.html" class="link">输出控制函数</a>。

<!-- -->

**我需要直接访问请求报头中的信息，怎么能办到？**  
如果以 Apache 的模块方式运行 PHP，那么函数 <span
class="function">getallheaders</span>
可以做这件事。因此下面的代码可以显示所有的请求报头：

``` php
<?php
$headers = getallheaders();
foreach ($headers as $name => $content) {
    echo "headers[$name] = $content<br />\n";
}
?>
```

请参阅函数 <span class="function">apache\_lookup\_uri</span>、 <span
class="function">apache\_response\_headers</span> 和 <span
class="function">fsockopen</span>。

<!-- -->

**当我用 IIS 进行 HTTP 认证时得到 “No Input file specified” 消息。**  
IIS 的安全模型这里有毛病。这是所有 IIS 下运行的 CGI
程序所共有的问题。一个解决办法是建立一个纯 HTML 文件（不经过 PHP
解析）作为要进入认证目录的登录页面，然后用 META 标记来重定向到 PHP
页面，或者用一个连接到 PHP 页面。然后 PHP
就可以正确识别认证信息了。如果是用 ISAPI 模块，那没有这个问题。其它 NT
下的 web 服务器不受此影响。更多信息见
<a href="http://support.microsoft.com/kb/q160422/" class="link external">» http://support.microsoft.com/kb/q160422/</a>
及 <a href="/features/http-auth.html" class="link">HTTP 认证</a> 一章。

<!-- -->

**Windows：不能访问另一台电脑上用 IIS 共享的文件。**  
必须要做些修改。打开 *Internet 信息服务*，找到你的 PHP
文件并打开属性页，选择 *文件安全性*标签，点击
*匿名访问和身份验证控制*的“编辑”按钮。

解决此问题有两个方法，一是不要选中 *匿名访问*并且选中 *集成 Windows
身份验证*，二是选中
*匿名访问*并编辑匿名访问使用的帐户，改成一个有权限的。

<!-- -->

**我怎样混合使用 XML 和 PHP？它不认我的 \<?xml 标记！**  
要能够在 PHP 代码中直接嵌入 \<?xml，需要将 PHP 设置项
<a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tags</a>设置为
*0*以关闭短标记格式。无法通过函数 <span
class="function">ini\_set</span>来更改这项设置。不管
<a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tags</a>是开或者关，都可以用类似于
*\<?php echo '\<?xml'; ?\>*的方法达到目的。该项设置的默认值为开。

<!-- -->

**哪里可以找到所有可用的 PHP 预定义变量的完整列表？**  
请阅读手册中的
<a href="/language/variables/predefined.html" class="link">预定义变量</a>
一章，该部分的文档已经包含了一部分可以用于你的脚本的预定义变量的列表。可用变量的完整列表（及更多信息）可以通过调用
<span class="function">phpinfo</span> 函数来查阅。请务必阅读手册中
<a href="/language/variables/external.html" class="link">来自 PHP 之外的变量</a>
一节，这部分文档阐述了外部变量的概念，例如来自 HTML 表单、Cookie 和 URL
的变量。

> **Note**: **register\_globals 重要说明：**  
>
> 自 PHP 4.2.0 起，PHP 指令
> <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
> 的默认值为 *off*。PHP 社区鼓励开发者不要依赖于此指令,
> 用其他手段替代，例如<a href="/language/variables/predefined.html" class="link">superglobals</a>。

<!-- -->

**怎样才能不用非免费的商业库（例如 <a href="/ref/pdf.html" class="link">PDFLib</a>） 来生成 PDF 文档？我想要个免费的并且不需要再连接别的 PDF 库。**  
有几个选择，例如
<a href="http://www.fpdf.org/" class="link external">» FPDF</a> 和
<a href="http://www.tcpdf.org/" class="link external">» TCPDF</a> 模块。

<!-- -->

**我试着在用户自定义函数中访问一个标准的 CGI 变量（例如 `$DOCUMENT_ROOT` 或 `$HTTP_REFERER`），但是找不到，哪里出了错？**  
首先非常重要的一点是 PHP 设置项
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
同样会对服务器端和环境变量产生影响。当 register\_globals = off （从 PHP
4.2.0 开始其默认值为 off），变量 `$DOCUMENT_ROOT` 将不会存在，而只有
`$_SERVER['DOCUMENT_ROOT']`。如果 register\_globals = on 则变量
`$DOCUMENT_ROOT` 和 `$GLOBALS['DOCUMENT_ROOT']` 将同时存在。

如果确认 register\_globals = on 但不知道为什么 `$DOCUMENT_ROOT`
在函数内部不可用，这是因为它和其它的变量一样需要在函数中执行 *global
$DOCUMENT\_ROOT*。请参阅手册中的
<a href="/language/variables/scope.html" class="link">变量范围</a>
一节。建议在 register\_globals = off 的情况下进行编码。

<!-- -->

**有些 PHP 选项可以接受缩写的字节值，与仅能接受 <span class="type">integer</span> 字节值相反。都有哪些缩写字节值？**  
可用的选择有 K（对应 Kilobytes），M（对应 Megabytes）和 G（对应
Gigabytes；自 PHP 5.1.0 起可用），区分大小写。其余的都认为是字节。
*1M*等于一个 Megabyte，即 *1048576* 字节。 *1K* 等于一个 Kilobyte，即
*1024* 字节。不能在 `php.ini` 之外使用这些符号，最好用整数的 <span
class="type">integer</span> 字节值。参见 <span
class="function">ini\_get</span> 文档中的转换示例。要注意，数字类型为
<span class="type">integer</span> 会自动取整，这意味着 *0.5M* 与 *0*
是等价的。

> **Note**: **kilobyte 和 kibibyte 的区别**  
>
> PHP 将一个千字节（kilobyte）描述为等于 1024 字节（bytes），而 IEC
> 标准则认为这是一个 kibibyte。结论：k 和 K = 1024 bytes.

<!-- -->

**在 Windows 下，使用 *localhost* 访问的时候提示连接超时，但是使用 *"127.0.0.1"* 的时候正常，为什么？**  
在 PHP 5.3.4 之前，如果启用了 IPv6，PHP 内部的网络解析代码有一个
bug，会导致处理 *localhost* 相关的地址时失败。可以通过使用 *"127.0.0.1"*
或在 `hosts` 文件中禁止 IPv6 来解决这个问题。
