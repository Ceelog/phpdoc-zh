现在，PHP
已经发展成为一种流行的脚本语言，可以在很多公共的资源里找到可以在自己的脚本中重新利用的代码。PHP
语言的开发者为向下兼容性下了很多功夫，因此在新版本的 PHP
下，老版本的代码应该可以在不作任何改动的情况下（理想地）运行。不过实际上，还是必须对老的代码做一些改动。

有可能影响到老版本的代码的最重要的两点改动分别是：

-   <span class="simpara"> 旧的 `$HTTP_*_VARS` 数组从 PHP 5.4.0
    开始将不再有效。 PHP
    <a href="https://www.php.net/releases/4_1_0.php" class="link external">» 4.1.0</a>
    版本引入了如下<a href="/language/variables/superglobals.html" class="link">超全局数组变量</a>：
    `$_GET`、`$_POST`、`$_COOKIE`、 `$_SERVER`、`$_FILES`、`$_ENV`、
    `$_REQUEST` 以及 `$_SESSION`。 </span>
-   <span class="simpara">
    外部变量不再被默认注册为全局变量。也就是说，从 PHP
    <a href="https://www.php.net/releases/4_2_0.php" class="link external">» 4.2.0</a>
    版开始，`php.ini` 中的设置选项
    <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
    默认值变成了
    *off*。建议用以上提到的超全局数组变量来访问这些值。但可能老的脚本、书籍以及教程都可能建立在该设置为
    on 的基础上。如果该选项被设置为 on，则可以在 URL
    *http://www.example.com/foo.php?id=42* 中直接使用变量
    `$id`。但不管被设置为 on 还是 off，`$_GET['id']` 一直有效。 </span>

如果希望了解关于这些改动的细节，请参阅“<a href="/language/variables/predefined.html" class="link">预定义变量</a>”一章以及其中的连接。
