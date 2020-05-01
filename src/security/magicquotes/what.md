什么是魔术引号
--------------

**Warning**

本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

当打开时，所有的 *'*（单引号），*"*（双引号），*\\*（反斜线）和 *NULL*
字符都会被自动加上一个反斜线进行转义。这和 <span
class="function">addslashes</span> 作用完全相同。

一共有三个魔术引号指令：

-   <span class="simpara">
    <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>
    </span> <span class="simpara"> 影响到 HTTP 请求数据（GET，POST 和
    COOKIE）。不能在运行时改变。在 PHP 中默认值为 *on*。 </span> <span
    class="simpara"> 参见 <span
    class="function">get\_magic\_quotes\_gpc</span>。 </span>
-   <span class="simpara">
    <a href="/info/setup.html#" class="link">magic_quotes_runtime</a>
    </span> <span class="simpara">
    如果打开的话，大部份从外部来源取得数据并返回的函数，包括从数据库和文本文件，所返回的数据都会被反斜线转义。该选项可在运行的时改变，在
    PHP 中的默认值为 *off*。 </span> <span class="simpara"> 参见 <span
    class="function">set\_magic\_quotes\_runtime</span> 和 <span
    class="function">get\_magic\_quotes\_runtime</span>。 </span>
-   <span class="simpara">
    <a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>
    </span> <span class="simpara">
    如果打开的话，将会使用单引号对单引号进行转义而非反斜线。此选项会完全覆盖
    <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>。如果同时打开两个选项的话，单引号将会被转义成
    *''*。而双引号、反斜线 和 NULL 字符将不会进行转义。 </span> <span
    class="simpara"> 如何取得其值参见 <span
    class="function">ini\_get</span>。 </span>
