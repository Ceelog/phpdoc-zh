不向下兼容的改变
----------------

尽管大部分 PHP 4
的代码应该不用修改就能运行，还是应该留意以下不向下兼容的改变：

-   <span class="simpara"> 有了一些
    <a href="/reserved/keywords.html" class="link">新关键字</a>。
    </span>
-   <span class="simpara"> <span class="function">strrpos</span> 和
    <span class="function">strripos</span> 如今使用整个字符串作为
    needle。 </span>
-   <span class="simpara"> 非法使用字符串偏移量会导致 **`E_ERROR`**
    而不是 **`E_WARNING`**。一个非法使用的例子： *$str = 'abc';
    unset($str\[0\]);*。 </span>
-   <span class="simpara"> <span class="function">array\_merge</span>
    被改成只接受数组。如果传递入非数组变量，对每个此类参数都会发出一条
    **`E_WARNING`** 信息。要小心因为你的代码有可能疯狂发出
    **`E_WARNING`**。 </span>
-   <span class="simpara"> PATH\_TRANSLATED 服务器变量在 Apache2 SAPI
    中不再暗中设定，这和 PHP 4 中的情形相反，如果 Apache
    没产生此值则其被设为和 SCRIPT\_FILENAME
    服务器变量一样的值。此修改是为了遵守
    <a href="http://www.faqs.org/rfcs/rfc3875" class="link external">» CGI 规范</a>。更多信息见
    <a href="https://bugs.php.net/23610" class="link external">» bug #23610</a>，并参考手册中
    <a href="/reserved/variables/server.html" class="link">$_SERVER['PATH_TRANSLATED']</a>
    的说明。此问题也影响到 PHP \>= 4.3.2 的版本。 </span>
-   <span class="simpara">
    <a href="/ref/tokenizer.html" class="link">Tokenizer</a>
    扩展不再定义 **`T_ML_COMMENT`** 常量。如果把 error\_reporting 设为
    **`E_ALL`**，PHP 将产生一条消息。尽管 **`T_ML_COMMENT`**
    从来都没用到过，还是在 PHP 4 中定义了。在 PHP 4 和 PHP 5 中 // 和
    /\* \*/ 都被解析为 **`T_COMMENT`** 常量。但是 PHPDoc 风格的注释
    /\*\* \*/，自 PHP 5 开始被 PHP 解析，被识别为 **`T_DOC_COMMENT`**。
    </span>
-   <span class="simpara"> 如果
    <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
    包括“S”，$\_SERVER 应该带有 argc 和 argv
    被产生。如果用户特别配制系统不创建
    $\_SERVER，那此变量当然就不存在了。改变的地方是不管
    <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
    怎么设定，在 CLI 版本中 argc 和 argv 总是可用的。本来 CLI
    版不是总会产生全局变量 $argc 和 $argv 的。 </span>
-   <span class="simpara"> 没有属性的对象不再被当成 “empty”。 </span>
-   <span class="simpara">
    有些情况下类必须在使用前被定义。这仅在使用了一些 PHP 5
    的新特性（例如
    <a href="/language/oop5/interfaces.html" class="link">interfaces</a>）的时候发生。其它情况下行为都没变。
    </span>
-   <span class="simpara"> <span
    class="function">get\_class</span>，<span
    class="function">get\_parent\_class</span> 和 <span
    class="function">get\_class\_methods</span>
    如今返回的类／方法名和定义时的名字一致（区分大小写），对于依赖以前行为（类／方法名总是返回小写的）的老脚本可能产生问题。一个可能的解决方法是在脚本中搜索所有这些函数并使用
    <span class="function">strtolower</span>。 </span> <span
    class="simpara">
    区分大小写的改变也适用于<a href="/language/constants/predefined.html" class="link">魔术常量</a>
    **`__CLASS__`**，**`__METHOD__`** 和
    **`__FUNCTION__`**。其值都会严格按照定义时的名字返回（区分大小写）。
    </span>
-   <span class="simpara"> <span class="function">ip2long</span>
    在传递入一个非法 IP 作为参数时返回 **`false`**，不再是 *-1*。
    </span>
-   <span class="simpara">
    如果有函数定义在包含文件中，则这些函数可以在主文件中使用而与是否在
    <span class="function">return</span>
    指令之前还是之后无关。如果文件被包含两次，PHP 5
    会发出致命错误，因为函数已经被定义，而 PHP 4 不管这个。因此推荐使用
    <span class="function">include\_once</span>
    而不要去检查文件是否已被包含以及在包含文件中有条件返回。 </span>
-   <span class="simpara"> <span class="function">include\_once</span>
    和 <span class="function">require\_once</span> 在 Windows
    下先将路径规格化，因此包含 A.php 和 a.php 只会把文件包含一次。
    </span>
-   <span class="simpara">
    将一个数组的值传递给一个函数，在函数内部访问数组时不再重置数组的内部指针。换句话说，在
    PHP 4
    中，当你把一个数组传给一个函数时，它在函数内部的指针会被重置，而在
    PHP 5
    中，当你把一个数组传给一个函数时，它在函数内部的数组指针会在传给函数时的位置。
    </span>

**示例 \#1 <span class="function">strrpos</span> 和 <span
class="function">strripos</span> 如今用整个字符串作为 needle**

``` php
<?php
var_dump(strrpos('ABCDEF','DEF')); //int(3)

var_dump(strrpos('ABCDEF','DAF')); //bool(false)
?>
```

**示例 \#2 没有属性的对象不再被当成“empty”**

``` php
<?php
class test { }
$t = new test();

var_dump(empty($t)); // echo bool(false)

if ($t) {
    // Will be executed
}
?>
```

**示例 \#3 有些情况下类必须在使用之前定义**

``` php
<?php

//works with no errors:
$a = new a();
class a {
}


//throws an error:
$a = new b();

interface c{
}
class b implements c {
}

?>
```
