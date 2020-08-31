对于全部脚本而言，PHP
提供了大量的预定义变量。这些变量将所有的<a href="/language/variables/external.html" class="link">外部变量</a>表示成内建环境变量，并且将错误信息表示成返回头。

参见 FAQ
“<a href="/faq/using.html#faq.register-globals" class="link">register_globals 对我有什么影响？</a>”

超全局变量
==========

超全局变量是在全部作用域中始终可用的内置变量

### 说明

PHP
中的许多预定义变量都是“超全局的”，这意味着它们在一个脚本的全部作用域中都可用。在函数或方法中无需执行
**global $variable;** 就可以访问它们。

这些超全局变量是：

-   `$GLOBALS`
-   `$_SERVER`
-   `$_GET`
-   `$_POST`
-   `$_FILES`
-   `$_COOKIE`
-   `$_SESSION`
-   `$_REQUEST`
-   `$_ENV`

### 注释

> **Note**: **变量可用性**  
>
> 默认情况下，所有的超全局变量都是可用的。但是，有一些指令会影响这种可用性。更多信息，参见文档
> <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>.

> **Note**: **处理 register\_globals**  
>
> 如果已经弃用的
> <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
> 指令被设置为 *on* 那么局部变量也将在脚本的全局作用域中可用。例如，
> `$_POST['foo']` 也将以 `$foo` 的形式存在。
>
> 相关信息，参见 FAQ
> “<a href="/faq/using.html#faq.register-globals" class="link">register_globals 对我有什么影响？</a>”

> **Note**: **可变变量**  
>
> 在函数或类方法中，超全局变量不能被用作<a href="/language/variables/variable.html" class="link">可变变量</a>。

### 参见

-   <a href="/language/variables/scope.html" class="link">变量作用域</a>
-   <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
    指令
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$GLOBALS
========

引用全局作用域中可用的全部变量

### 说明

一个包含了全部变量的全局组合<span
class="type">数组</span>。变量的名字就是数组的键。

### 范例

**示例 \#1 `$GLOBALS` 范例**

``` php
<?php
function test() {
    $foo = "local variable";

    echo '$foo in global scope: ' . $GLOBALS["foo"] . "\n";
    echo '$foo in current scope: ' . $foo . "\n";
}

$foo = "Example content";
test();
?>
```

以上例程的输出类似于：

    $foo in global scope: Example content
    $foo in current scope: local variable

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

> **Note**: **变量可用性**  
>
> 与所有其他<a href="/language/variables/superglobals.html" class="link">超全局变量</a>不同，`$GLOBALS`在PHP中总是可用的。

$\_SERVER
=========

$HTTP\_SERVER\_VARS \[已删除\]
==============================

服务器和执行环境信息

### 说明

`$_SERVER`
是一个包含了诸如头信息(header)、路径(path)、以及脚本位置(script
locations)等等信息的数组。这个数组中的项目由 Web
服务器创建。不能保证每个服务器都提供全部项目；服务器可能会忽略一些，或者提供一些没有在这里列举出来的项目。这也就意味着大量的此类变量都会在<a href="http://www.faqs.org/rfcs/rfc3875" class="link external">» CGI 1.1 规范</a>中说明，所以应该仔细研究一下。

> **Note**: <span class="simpara"> PHP 5.4.0 之前，`$HTTP_SERVER_VARS`
> 包含着相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
> (注意 `$HTTP_SERVER_VARS` 与 `$_SERVER`
> 是不同的变量，PHP处理它们的方式不同) </span>

### 目录

在 `$_SERVER`
中，你也许能够，也许不能够找到下面的这些元素。注意，如果以<a href="/features/commandline.html" class="link">命令行</a>方式运行
PHP，下面列出的元素几乎没有有效的(或是没有任何实际意义的)。

'`PHP_SELF`'  
<span class="simpara"> 当前执行脚本的文件名，与 document root
有关。例如，在地址为 `http://example.com/foo/bar.php` 的脚本中使用
`$_SERVER['PHP_SELF']` 将得到
`/foo/bar.php`。<a href="/language/constants/predefined.html" class="link">__FILE__</a>
常量包含当前(例如包含)文件的完整路径和文件名。 </span> <span
class="simpara"> 从 PHP 4.3.0 版本开始，如果 PHP
以命令行模式运行，这个变量将包含脚本名。之前的版本该变量不可用。 </span>

'<a href="/reserved/variables/argv.html" class="link">argv</a>'  
<span class="simpara">
传递给该脚本的参数的数组。当脚本以命令行方式运行时，argv 变量传递给程序
C 语言样式的命令行参数。当通过 GET 方式调用时，该变量包含query string。
</span>

'<a href="/reserved/variables/argc.html" class="link">argc</a>'  
<span class="simpara">
包含命令行模式下传递给该脚本的参数的数目(如果运行在命令行模式下)。
</span>

'`GATEWAY_INTERFACE`'  
<span class="simpara"> 服务器使用的 CGI 规范的版本；例如，“*CGI/1.1*”。
</span>

'`SERVER_ADDR`'  
<span class="simpara"> 当前运行脚本所在的服务器的 IP 地址。 </span>

'`SERVER_NAME`'  
<span class="simpara">
当前运行脚本所在的服务器的主机名。如果脚本运行于虚拟主机中，该名称是由那个虚拟主机所设置的值决定。
</span>

> **Note**: <span class="simpara"> 在 Apache 2 里，必须设置
> *UseCanonicalName = On* 和 *ServerName*。
> 否则该值会由客户端提供，就有可能被伪造。
> 上下文有安全性要求的环境里，不应该依赖此值。 </span>

'`SERVER_SOFTWARE`'  
<span class="simpara"> 服务器标识字符串，在响应请求时的头信息中给出。
</span>

'`SERVER_PROTOCOL`'  
<span class="simpara">
请求页面时通信协议的名称和版本。例如，“HTTP/1.0”。 </span>

'`REQUEST_METHOD`'  
<span class="simpara"> 访问页面使用的请求方法；例如，“*GET*”,
“*HEAD*”，“*POST*”，“*PUT*”。 </span>

> **Note**:
>
> 如果请求方法为 *HEAD*，PHP 脚本将在发送 Header
> 头信息之后终止(这意味着在产生任何输出后，不再有输出缓冲)。

'`REQUEST_TIME`'  
<span class="simpara"> 请求开始时的时间戳。从 PHP 5.1.0 起可用。 </span>

'`REQUEST_TIME_FLOAT`'  
<span class="simpara"> 请求开始时的时间戳，微秒级别的精准度。 自 PHP
5.4.0 开始生效。 </span>

'`QUERY_STRING`'  
<span class="simpara"> query
string（查询字符串），如果有的话，通过它进行页面访问。 </span>

'`DOCUMENT_ROOT`'  
<span class="simpara">
当前运行脚本所在的文档根目录。在服务器配置文件中定义。 </span>

'`HTTP_ACCEPT`'  
<span class="simpara"> 当前请求头中 *Accept:* 项的内容，如果存在的话。
</span>

'`HTTP_ACCEPT_CHARSET`'  
<span class="simpara"> 当前请求头中 *Accept-Charset:*
项的内容，如果存在的话。例如：“*iso-8859-1,\*,utf-8*”。 </span>

'`HTTP_ACCEPT_ENCODING`'  
<span class="simpara"> 当前请求头中 *Accept-Encoding:*
项的内容，如果存在的话。例如：“*gzip*”。 </span>

'`HTTP_ACCEPT_LANGUAGE`'  
<span class="simpara"> 当前请求头中 *Accept-Language:*
项的内容，如果存在的话。例如：“*en*”。 </span>

'`HTTP_CONNECTION`'  
<span class="simpara"> 当前请求头中 *Connection:*
项的内容，如果存在的话。例如：“*Keep-Alive*”。 </span>

'`HTTP_HOST`'  
<span class="simpara"> 当前请求头中 *Host:* 项的内容，如果存在的话。
</span>

'`HTTP_REFERER`'  
<span class="simpara">
引导用户代理到当前页的前一页的地址（如果存在）。由 user agent
设置决定。并不是所有的用户代理都会设置该项，有的还提供了修改
`HTTP_REFERER` 的功能。简言之，该值并不可信。 </span>

'`HTTP_USER_AGENT`'  
<span class="simpara"> 当前请求头中 *User-Agent:*
项的内容，如果存在的话。该字符串表明了访问该页面的用户代理的信息。一个典型的例子是：<span
class="computeroutput">Mozilla/4.5 \[en\] (X11; U; Linux 2.2.9
i586)</span>。除此之外，你可以通过 <span
class="function">get\_browser</span>
来使用该值，从而定制页面输出以便适应用户代理的性能。 </span>

'`HTTPS`'  
<span class="simpara"> 如果脚本是通过 HTTPS
协议被访问，则被设为一个非空的值。 </span>

> **Note**: <span class="simpara"> 注意当使用 IIS 上的 ISAPI
> 方式时，如果不是通过 HTTPS 协议被访问，这个值将为 *off*。 </span>

'`REMOTE_ADDR`'  
<span class="simpara"> 浏览当前页面的用户的 IP 地址。 </span>

'`REMOTE_HOST`'  
<span class="simpara"> 浏览当前页面的用户的主机名。DNS
反向解析不依赖于用户的 `REMOTE_ADDR`。 </span>

> **Note**: <span class="simpara">
> 你的服务器必须被配置以便产生这个变量。例如在 Apache 中，你需要在
> `httpd.conf` 中设置 *HostnameLookups On* 来产生它。参见 <span
> class="function">gethostbyaddr</span>。 </span>

'`REMOTE_PORT`'  
<span class="simpara"> 用户机器上连接到 Web 服务器所使用的端口号。
</span>

'`REMOTE_USER`'  
<span class="simpara"> 经验证的用户 </span>

'`REDIRECT_REMOTE_USER`'  
<span class="simpara"> 验证的用户，如果请求已在内部重定向。 </span>

'`SCRIPT_FILENAME`'  
当前执行脚本的绝对路径。

> **Note**:
>
> 如果在命令行界面（Command Line Interface,
> CLI）使用相对路径执行脚本，例如 `file.php` 或 `../file.php`，那么
> `$_SERVER['SCRIPT_FILENAME']` 将包含用户指定的相对路径。

'`SERVER_ADMIN`'  
<span class="simpara"> 该值指明了 Apache 服务器配置文件中的
SERVER\_ADMIN
参数。如果脚本运行在一个虚拟主机上，则该值是那个虚拟主机的值。 </span>

'`SERVER_PORT`'  
<span class="simpara"> Web 服务器使用的端口。默认值为 “*80*”。如果使用
SSL 安全连接，则这个值为用户设置的 HTTP 端口。 </span>

> **Note**: <span class="simpara"> 在 Apache 2
> 里，为了获取真实物理端口，必须设置 *UseCanonicalName = On* 以及
> *UseCanonicalPhysicalPort = On*。
> 否则此值可能被伪造，不一定会返回真实端口值。
> 上下文有安全性要求的环境里，不应该依赖此值。 </span>

'`SERVER_SIGNATURE`'  
<span class="simpara"> 包含了服务器版本和虚拟主机名的字符串。 </span>

'`PATH_TRANSLATED`'  
<span class="simpara">
当前脚本所在文件系统（非文档根目录）的基本路径。这是在服务器进行虚拟到真实路径的映像后的结果。
</span>

> **Note**: <span class="simpara"> 自 PHP 4.3.2 起，`PATH_TRANSLATED` 在
> Apache 2 SAPI 模式下不再和 Apache 1 一样隐含赋值，而是若 Apache
> 不生成此值，PHP 便自己生成并将其值放入 `SCRIPT_FILENAME`
> 服务器常量中。这个修改遵守了 CGI 规范，`PATH_TRANSLATED` 仅在
> `PATH_INFO` 被定义的条件下才存在。 </span> <span class="simpara">
> Apache 2 用户可以在 `httpd.conf` 中设置 *AcceptPathInfo = On* 来定义
> `PATH_INFO`。 </span>

'`SCRIPT_NAME`'  
<span class="simpara">
包含当前脚本的路径。这在页面需要指向自己时非常有用。<a href="/language/constants/predefined.html" class="link">__FILE__</a>
常量包含当前脚本(例如包含文件)的完整路径和文件名。 </span>

'`REQUEST_URI`'  
<span class="simpara"> URI 用来指定要访问的页面。例如 “*/index.html*”。
</span>

'`PHP_AUTH_DIGEST`'  
<span class="simpara"> 当作为 Apache 模块运行时，进行 HTTP Digest
认证的过程中，此变量被设置成客户端发送的“Authorization” HTTP
头内容（以便作进一步的认证操作）。 </span>

'`PHP_AUTH_USER`'  
<span class="simpara"> 当 PHP 运行在 Apache 或 IIS（PHP 5 是
ISAPI）模块方式下，并且正在使用 HTTP
认证功能，这个变量便是用户输入的用户名。 </span>

'`PHP_AUTH_PW`'  
<span class="simpara"> 当 PHP 运行在 Apache 或 IIS（PHP 5 是
ISAPI）模块方式下，并且正在使用 HTTP
认证功能，这个变量便是用户输入的密码。 </span>

'`AUTH_TYPE`'  
<span class="simpara"> 当 PHP 运行在 Apache 模块方式下，并且正在使用
HTTP 认证功能，这个变量便是认证的类型。 </span>

'`PATH_INFO`'  
<span class="simpara">
包含由客户端提供的、跟在真实脚本名称之后并且在查询语句（query
string）之前的路径信息，如果存在的话。例如，如果当前脚本是通过 URL
`http://www.example.com/php/path_info.php/some/stuff?foo=bar`
被访问，那么 `$_SERVER['PATH_INFO']` 将包含 */some/stuff*。 </span>

'`ORIG_PATH_INFO`'  
<span class="simpara"> 在被 PHP 处理之前，“`PATH_INFO`” 的原始版本。
</span>

### 更新日志

| 版本  | 说明                                                                                                                               |
|-------|------------------------------------------------------------------------------------------------------------------------------------|
| 5.4.0 | 因为移除了 long array register 功能，`$HTTP_SERVER_VARS` 不再有效。                                                                |
| 5.3.0 | 废弃了使 `$HTTP_SERVER_VARS` 生效的 <a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a> 指令。 |

### 范例

**示例 \#2 `$_SERVER` 范例**

``` php
<?php
echo $_SERVER['SERVER_NAME'];
?>
```

以上例程的输出类似于：

    www.example.com

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$\_GET
======

$HTTP\_GET\_VARS \[已弃用\]
===========================

HTTP GET 变量

### 说明

通过 URL 参数（又叫 query string）传递给当前脚本的变量的数组。
注意：该数组不仅仅对 method 为 GET 的请求生效，而是会针对所有带 query
string 的请求。

`$HTTP_GET_VARS` 包含相同的信息，
但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_GET_VARS` 和 `$_GET` 是不同的变量，PHP 处理它们的方式不同)

### 范例

**示例 \#3 `$_GET` 范例**

``` php
<?php
echo 'Hello ' . htmlspecialchars($_GET["name"]) . '!';
?>
```

假设用户访问的是 http://example.com/?name=Hannes

以上例程的输出类似于：

    Hello Hannes!

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

> **Note**:
>
> GET 是通过 <span class="function">urldecode</span> 传递的。

### 参见

-   <a href="/language/variables/external.html" class="link">处理外部变量</a>
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$\_POST
=======

$HTTP\_POST\_VARS \[已弃用\]
============================

HTTP POST 变量

### 说明

当 HTTP POST 请求的 Content-Type 是 *application/x-www-form-urlencoded*
或 *multipart/form-data* 时，会将变量以关联数组形式传入当前脚本。

`$HTTP_POST_VARS`
包含相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_POST_VARS` 和 `$_POST` 是不同的变量，PHP
处理它们的方式不同)

### 范例

**示例 \#4 `$_POST` 范例**

``` php
<?php
echo 'Hello ' . htmlspecialchars($_POST["name"]) . '!';
?>
```

假设用户通过 HTTP POST 方式传递了参数 name=Hannes

以上例程的输出类似于：

    Hello Hannes!

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <a href="/language/variables/external.html" class="link">处理外部变量</a>
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$\_FILES
========

$HTTP\_POST\_FILES \[已弃用\]
=============================

HTTP 文件上传变量

### 说明

通过 HTTP POST 方式上传到当前脚本的项目的<span
class="type">数组</span>。 此数组的概况在
<a href="/features/file-upload/post-method.html" class="link">POST 方法上传</a>
章节中有描述。

`$HTTP_POST_FILES`
包含相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_POST_FILES` 和 `$_FILES` 是不同的变量，PHP
处理它们的方式不同)

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <span class="function">move\_uploaded\_file</span>
-   <a href="/features/file-upload.html" class="link">处理文件上传</a>

$\_REQUEST
==========

HTTP Request 变量

### 说明

默认情况下包含了 `$_GET`，`$_POST` 和 `$_COOKIE` 的<span
class="type">数组</span>。

### 更新日志

| 版本  | 说明                                                                                                              |
|-------|-------------------------------------------------------------------------------------------------------------------|
| 5.3.0 | 引入 <a href="/ini/core.html#ini.request-order" class="link">request_order</a>。该指令会影响 `$_REQUEST` 的内容。 |

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

> **Note**:
>
> 以<a href="/features/commandline.html" class="link">命令行</a>方式运行时，将*不*包含
> <a href="/reserved/variables/argv.html" class="link">argv</a> 和
> <a href="/reserved/variables/argc.html" class="link">argc</a>
> 信息；它们将存在于 `$_SERVER` <span class="type">数组</span>。

> **Note**:
>
> 由于 `$_REQUEST` 中的变量通过 GET，POST 和 COOKIE
> 输入机制传递给脚本文件，因此可以被远程用户篡改而并不可信。这个数组的项目及其顺序依赖于
> PHP 的
> <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
> 指令的配置。

### 参见

-   <span class="function">import\_request\_variables</span>
-   <a href="/language/variables/external.html" class="link">处理外部变量</a>
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$\_SESSION
==========

$HTTP\_SESSION\_VARS \[已弃用\]
===============================

Session 变量

### 说明

当前脚本可用 SESSION 变量的数组。更多关于如何使用的信息，参见
<a href="/ref/session.html" class="link">Session 函数</a> 文档。

`$HTTP_SESSION_VARS`
包含相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_SESSION_VARS` 和 `$_SESSION` 是不同的变量，PHP
处理它们的方式不同)

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <span class="function">session\_start</span>

$\_ENV
======

$HTTP\_ENV\_VARS \[已弃用\]
===========================

环境变量

### 说明

通过环境方式传递给当前脚本的变量的<span class="type">数组</span>。

这些变量被从 PHP 解析器的运行环境导入到 PHP 的全局命名空间。很多是由支持
PHP 运行的 Shell 提供的，并且不同的系统很可能运行着不同种类的
Shell，所以不可能有一份确定的列表。请查看你的 Shell
文档来获取定义的环境变量列表。

其他环境变量包含了 CGI 变量，而不管 PHP 是以服务器模块还是 CGI
处理器的方式运行。

`$HTTP_ENV_VARS`
包含相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_ENV_VARS` 和 `$_ENV` 是不同的变量，PHP 处理它们的方式不同)

### 范例

**示例 \#5 `$_ENV` 范例**

``` php
<?php
echo 'My username is ' .$_ENV["USER"] . '!';
?>
```

假设 "bjori" 运行此段脚本

以上例程的输出类似于：

    My username is bjori!

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <span class="function">getenv</span>
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$\_COOKIE
=========

$HTTP\_COOKIE\_VARS \[已弃用\]
==============================

HTTP Cookies

### 说明

通过 HTTP Cookies 方式传递给当前脚本的变量的<span
class="type">数组</span>。

`$HTTP_COOKIE_VARS`
包含相同的信息，但它不是一个<a href="/language/variables/superglobals.html" class="link">超全局变量</a>。
(注意 `$HTTP_COOKIE_VARS` 和 `$_COOKIE` 是不同的变量，PHP
处理它们的方式不同)

### 范例

**示例 \#6 `$_COOKIE` 范例**

``` php
<?php
echo 'Hello ' . htmlspecialchars($_COOKIE["name"]) . '!';
?>
```

假设之前发送了 "name" Cookie

以上例程的输出类似于：

    Hello Hannes!

### 注释

> **Note**:
>
> “Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用
> **global $variable;** 来访问它。

### 参见

-   <span class="function">setcookie</span>
-   <a href="/language/variables/external.html" class="link">处理外部变量</a>
-   <a href="/book/filter.html" class="link">过滤器扩展</a>

$php\_errormsg
==============

前一个错误信息

**Warning**

本特性已自 PHP 7.2.0 起*废弃*。强烈建议不要使用本特性。

用 <span class="function">error\_get\_last</span> 函数代替。

### 说明

`$php_errormsg` 变量包含由 PHP
生成的最新错误信息。这个变量只在错误发生的作用域内可用，并且要求
<a href="/errorfunc/setup.html#" class="link">track_errors</a>
配置项是开启的（默认是关闭的）。

**Warning**

如果用户定义了错误处理句柄（<span
class="function">set\_error\_handler</span>）并且返回 **`FALSE`**
的时候，`$php_errormsg` 就会被设置。

### 范例

**示例 \#7 `$php_errormsg` 范例**

``` php
<?php
@strpos();
echo $php_errormsg;
?>
```

以上例程的输出类似于：

    Wrong parameter count for strpos()

### 参见

-   <span class="function">error\_get\_last</span>

$HTTP\_RAW\_POST\_DATA
======================

原生POST数据

### 说明

**Warning**

This feature was *DEPRECATED* in PHP 5.6.0, and *REMOVED* as of PHP
7.0.0.

`$HTTP_RAW_POST_DATA` 包含 POST 提交的原始数据。参见
<a href="/ini/core.html#ini.always-populate-raw-post-data" class="link">always_populate_raw_post_data</a>

一般而言，使用
<a href="/wrappers/php.html#wrappers.php.input" class="link"><em>php://input</em></a>
代替 `$HTTP_RAW_POST_DATA`。

$http\_response\_header
=======================

HTTP 响应头

### 说明

`$http_response_header` <span class="type">数组</span>与 <span
class="function">get\_headers</span>
函数类似。当使用<a href="/wrappers/http.html" class="link">HTTP 包装器</a>时，`$http_response_header`
将会被 HTTP 响应头信息填充。`$http_response_header`
将被创建于<a href="/language/variables/scope.html" class="link">局部作用域</a>中。

### 范例

**示例 \#8 `$http_response_header` 范例**

``` php
<?php
function get_contents() {
  file_get_contents("http://example.com");
  var_dump($http_response_header);
}
get_contents();
var_dump($http_response_header);
?>
```

以上例程的输出类似于：

    array(9) {
      [0]=>
      string(15) "HTTP/1.1 200 OK"
      [1]=>
      string(35) "Date: Sat, 12 Apr 2008 17:30:38 GMT"
      [2]=>
      string(29) "Server: Apache/2.2.3 (CentOS)"
      [3]=>
      string(44) "Last-Modified: Tue, 15 Nov 2005 13:24:10 GMT"
      [4]=>
      string(27) "ETag: "280100-1b6-80bfd280""
      [5]=>
      string(20) "Accept-Ranges: bytes"
      [6]=>
      string(19) "Content-Length: 438"
      [7]=>
      string(17) "Connection: close"
      [8]=>
      string(38) "Content-Type: text/html; charset=UTF-8"
    }
    NULL

$argc
=====

传递给脚本的参数数目

### 说明

包含当运行于<a href="/features/commandline.html" class="link">命令行</a>下时传递给当前脚本的参数的数目。

> **Note**: <span class="simpara">
> 脚本的文件名总是作为参数传递给当前脚本，因此 `$argc` 的最小值为 *1*。
> </span>

> **Note**: <span class="simpara"> 这个变量仅在
> <a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>
> 打开时可用。 </span>

### 范例

**示例 \#9 `$argc` 范例**

``` php
<?php
var_dump($argc);
?>
```

当使用这个命令执行: php script.php arg1 arg2 arg3

以上例程的输出类似于：

    int(4)

### 注释

> **Note**:
>
> 也可以在 `$_SERVER['argc']` 中获取。

### 参见

-   <span class="function">getopt</span>
-   <a href="/reserved/variables/argv.html" class="link"><var class="varname">$argv</var></a>

$argv
=====

传递给脚本的参数数组

### 说明

包含当运行于<a href="/features/commandline.html" class="link">命令行</a>下时传递给当前脚本的参数的数组。

> **Note**: <span class="simpara"> 第一个参数总是当前脚本的文件名，因此
> `$argv[0]` 就是脚本文件名。 </span>

> **Note**: <span class="simpara"> 这个变量仅在
> <a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>
> 打开时可用。 </span>

### 范例

**示例 \#10 `$argv` 范例**

``` php
<?php
var_dump($argv);
?>
```

当使用这个命令执行：php script.php arg1 arg2 arg3

以上例程的输出类似于：

    array(4) {
      [0]=>
      string(10) "script.php"
      [1]=>
      string(4) "arg1"
      [2]=>
      string(4) "arg2"
      [3]=>
      string(4) "arg3"
    }

### 参见

-   <span class="function">getopt</span>

**目录**

-   [超全局变量](/language/variables/superglobals.html) —
    超全局变量是在全部作用域中始终可用的内置变量
-   [$GLOBALS](/reserved/variables/globals.html) —
    引用全局作用域中可用的全部变量
-   [$\_SERVER](/reserved/variables/server.html) — 服务器和执行环境信息
-   [$\_GET](/reserved/variables/get.html) — HTTP GET 变量
-   [$\_POST](/reserved/variables/post.html) — HTTP POST 变量
-   [$\_FILES](/reserved/variables/files.html) — HTTP 文件上传变量
-   [$\_REQUEST](/reserved/variables/request.html) — HTTP Request 变量
-   [$\_SESSION](/reserved/variables/session.html) — Session 变量
-   [$\_ENV](/reserved/variables/environment.html) — 环境变量
-   [$\_COOKIE](/reserved/variables/cookies.html) — HTTP Cookies
-   [$php\_errormsg](/reserved/variables/phperrormsg.html) —
    前一个错误信息
-   [$HTTP\_RAW\_POST\_DATA](/reserved/variables/httprawpostdata.html) —
    原生POST数据
-   [$http\_response\_header](/reserved/variables/httpresponseheader.html)
    — HTTP 响应头
-   [$argc](/reserved/variables/argc.html) — 传递给脚本的参数数目
-   [$argv](/reserved/variables/argv.html) — 传递给脚本的参数数组
