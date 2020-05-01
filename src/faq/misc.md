其他问题
========

有些问题没法归到其它类中，可以在这里找到。

1.  [在 Windows 中怎样处理 bz2 压缩的文档？](#faq.misc.bz2)
2.  [在函数定义中，参数旁边的 & 是什么意思？例如
    asort。](#faq.misc.arguments.references)
3.  [怎么处理 register\_globals？](#faq.misc.registerglobals)

**在 Windows 中怎样处理 bz2 压缩的文档？**  
如果没有能处理 bz2 文件的压缩工具，从 Redhat
<a href="https://www.sourceware.org/bzip2/" class="link external">» 下载</a>一个命令行工具（进一步信息见下面）。

如果不喜欢用命令行工具，可以试试免费工具例如
<a href="http://www.stuffit.com/" class="link external">» Stuffit Expander</a>，
<a href="http://www.ultimatezip.com/" class="link external">» UltimateZip</a>，
<a href="http://www.7-zip.org/" class="link external">» 7-Zip</a>或者
<a href="http://www.quickzip.org/" class="link external">» Quick Zip</a>。如果有像
<a href="http://www.rarlab.com/" class="link external">» WinRAR</a>或者
<a href="http://www.powerarchiver.com/" class="link external">» Power Archiver</a>之类的工具，可以很容易用它解压缩
bz2 文件。如果用 Total Commander（前身为 Windows Commander），可以从
<a href="http://www.ghisler.com/" class="link external">» Total Commander</a>网站免费得到一个
bz2 插件。

来自 Redhat 的 bzip2 命令行工具：

Win2K Sp2 用户下载最新版本 1.0.2，所有其它 Windows 用户应该用版本
1.00。下载后重命名可执行文件为
bzip2.exe。为方便起见将其放到一个在你路径中的目录，例如 C:\\Windows，C
表示你安装 Windows 的盘符。

注意：lang 指的是你的语种，x 是想要的格式，例如：pdf。要解压缩
php\_manual\_lang.x.bz2，按照下面的简单说明进行：

-   <span class="simpara">打开一个命令行窗口</span>
-   <span class="simpara">进入存放已下载的 php\_manual\_lang.x.bz2
    的目录</span>
-   <span class="simpara">调用 bzip2 -d php\_manual\_lang.x.bz2，将
    php\_manual\_lang.x 释放到同一个目录</span>

在下载了包含很多 html 文件的 php\_manual\_lang.tar.bz2
的情况下，过程是一样的。唯一区别是得到了一个 php\_manual\_lang.tar
文件。tar 格式可以被大多数 Windows 下流行的压缩工具所处理，例如
<a href="http://www.winzip.com/" class="link external">» WinZip</a>。

<!-- -->

**在函数定义中，参数旁边的 & 是什么意思？例如 <span class="function">asort</span>。**  
这表示该参数是
<a href="/language/references/pass.html" class="link">引用传递</a>，该函数会修改其值。只可以用此方法传递变量，其实都不需要在函数调用中用
& 传递（此方式都已
<a href="/ini/core.html#ini.allow-call-time-pass-reference" class="link">过时了</a>）。

<!-- -->

**怎么处理 *register\_globals*？**  
有关 *register\_globals*实现方面的安全性，请阅读
<a href="/security/globals.html" class="link">使用 register_globals</a>一章。

推荐使用
<a href="/language/variables/superglobals.html" class="link">超全局变量</a>而不要依赖
*register\_globals*。

如果需要在一台关闭了
*register\_globals*的共享主机上运行一些旧式程序而该程序需要此选项打开时，或者在一些打开了此选项的主机上但想消除安全隐患，那么就需要用
PHP 来模拟出相反的设定。最好先问清楚是否能否在哪里更改 PHP
配置的选项，如果不行，那可以用如下的兼容手段。

**示例 \#1 模拟注册全局变量**

本例模拟 register\_globals On。如果改变了配置文件中的
<a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>选项，则考虑对
`$superglobals`作出相应的改动。

``` php
<?php
// Emulate register_globals on
if (!ini_get('register_globals')) {
    $superglobals = array($_SERVER, $_ENV,
        $_FILES, $_COOKIE, $_POST, $_GET);
    if (isset($_SESSION)) {
        array_unshift($superglobals, $_SESSION);
    }
    foreach ($superglobals as $superglobal) {
        extract($superglobal, EXTR_SKIP);
    }
}
?>
```

本例模拟 register\_globals
Off。要记住此代码应在脚本最开头的地方调用。如果使用了会话机制，则在
<span class="function">session\_start</span>之后调用。

``` php
<?php
// Emulate register_globals off
function unregister_GLOBALS()
{
    if (!ini_get('register_globals')) {
        return;
    }

    // Might want to change this perhaps to a nicer error
    if (isset($_REQUEST['GLOBALS']) || isset($_FILES['GLOBALS'])) {
        die('GLOBALS overwrite attempt detected');
    }

    // Variables that shouldn't be unset
    $noUnset = array('GLOBALS',  '_GET',
                     '_POST',    '_COOKIE',
                     '_REQUEST', '_SERVER',
                     '_ENV',     '_FILES');

    $input = array_merge($_GET,    $_POST,
                         $_COOKIE, $_SERVER,
                         $_ENV,    $_FILES,
                         isset($_SESSION) && is_array($_SESSION) ? $_SESSION : array());

    foreach ($input as $k => $v) {
        if (!in_array($k, $noUnset) && isset($GLOBALS[$k])) {
            unset($GLOBALS[$k]);
        }
    }
}

unregister_GLOBALS();

?>
```
