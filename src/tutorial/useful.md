现在来编写一些更实用的脚本，比如检查浏览页面的访问者在用什么浏览器。要达到这个目的，需要检查用户的
agent 字符串，它是浏览器发送的 HTTP
请求的一部分。该信息被存储在一个<a href="/language/variables.html" class="link">变量</a>中。在
PHP 中，变量总是以一个美元符开头。我们现在感兴趣的变量是
`$_SERVER['HTTP_USER_AGENT']`。

> **Note**:
>
> <a href="/reserved/variables/server.html" class="link">$_SERVER</a>
> 是一个特殊的 PHP 保留变量，它包含了 web
> 服务器提供的所有信息，被称为超全局变量。请查阅本手册“<a href="/language/variables/superglobals.html" class="link">超全局变量</a>”中的有关内容以获取更多信息。这些特殊的变量是在
> PHP
> <a href="https://www.php.net/releases/4_1_0.php" class="link external">» 4.1.0</a>
> 版本引入的。在这之前使用 `$HTTP_*_VARS` 数组，如
> `$HTTP_SERVER_VARS`。尽管现在已经不用了，但它们在新版本中仍然存在（参见“<a href="/tutorial/oldcode.html" class="link">旧代码</a>”一节中的注解）。

要显示该变量，只需简单地进行如下操作：

**示例 \#1 打印一个变量（数组元素）**

``` php
<?php 
echo $_SERVER['HTTP_USER_AGENT']; 
?>
```

该脚本的输出可能是：

  
Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1)  

PHP
有很多种不同<a href="/language/types.html" class="link">类型</a>的变量。在以上例子中我们打印了一个<a href="/language/types/array.html" class="link">数组</a>的单元。数组是一类非常有用的变量。

`$_SERVER` 只是 PHP
自动全局化的变量之一。可以查阅“<a href="/reserved/variables.html" class="link">预定义变量</a>”一节来查看这些变量的列表，或者也可以通过上节例子中
<span class="function">phpinfo</span> 函数的输出来查看。

可以在一个 PHP 标识中加入多个 PHP 语句，也可以建立一个代码块来做比简单的
echo 更多的事情。例如，如果需要识别 Internet
Explorer，可以进行如下操作：

**示例 \#2
<a href="/language/control-structures.html" class="link">流程控制</a>与<a href="/language/functions.html" class="link">函数</a>的使用**

``` php
<?php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
    echo '正在使用 Internet Explorer。<br />';
}
?>
```

该脚本的输出可能是：

    正在使用 Internet Explorer。<br />

这里要介绍一些新的原理。上面用了一个
<a href="/control-structures/if.html" class="link">if</a>
语句。如果用户对 C
语言的基本语法比较熟悉，则应该对此很熟悉，否则，可能需要拿起任何一本 PHP
介绍性的书籍并阅读前面的两三个章节，或者也可以阅读本手册的“<a href="/langref.html" class="link">语言参考</a>”一章。

需要介绍的第二个原理，是对 <span class="function">strpos</span>
函数的调用。<span class="function">strpos</span> 是 PHP
的一个内置函数，其功能是在一个字符串中搜索另外一个字符串。例如我们现在需要在
`$_SERVER['HTTP_USER_AGENT']`（即所谓的 haystack）变量中寻找
*'MSIE'*。如果在这个 haystack 中该字符串（即所谓的
needle）被找到（“草里寻针”），则函数返回 needle 在 haystack
中相对于开头的位置；如果没有，则返回 **`false`**。如果该函数没有返回
**`false`**，则
<a href="/control-structures/if.html" class="link">if</a> 会将条件判断为
**`true`** 并运行其花括号 {}
内的代码；否则，则不运行这些代码。可以自己尝试利用
<a href="/control-structures/if.html" class="link">if</a>，<a href="/control-structures/else.html" class="link">else</a>
以及其它的函数如 <span class="function">strtoupper</span> 和 <span
class="function">strlen</span>
来建立类似的脚本。在本手册中相关的页面也包含有范例。如果对如何使用函数不是很确定，可以阅读手册中有关“<a href="/about/prototypes.html" class="link">如何阅读函数的定义</a>”和“<a href="/language/functions.html" class="link">函数</a>”的有关章节。

以下我们进一步显示如何进出 PHP 模式，甚至是在一个 PHP 代码块的中间：

**示例 \#3 混和 HTML 和 PHP 模式**

``` php
<?php
if (strpos($_SERVER['HTTP_USER_AGENT'], 'MSIE') !== FALSE) {
?>
<h3>strpos() 肯定没有返回假 (FALSE)</h3>
<p>正在使用 Internet Explorer</p>
<?php
} else {
?>
<h3>strpos() 肯定返回假 (FALSE)</h3>
<center><b>没有使用 Internet Explorer</b></center>
<?php
}
?>
```

该脚本的输出可能是：

    <h3>strpos() 肯定没有返回假 (FALSE)</h3>
    <p>正在使用 Internet Explorer</p>

和以上我们用一个 PHP 的 echo 语句来输出不同的是，我们跳出了 PHP
模式来直接写 HTML
代码。这里很值得注意的一点是，对于这两种情况而言，脚本的逻辑效率是相同的。在判断了
<span class="function">strpos</span> 函数的返回值是 **`true`** 或是
**`false`**，也就是判断了字符串 *'MSIE'* 是否被找到之后，最终只有一个
HTML 块被发送给浏览者。
