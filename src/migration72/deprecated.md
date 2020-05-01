PHP 7.2.x 中废弃的功能
----------------------

### 不带引号的字符串

不带引号的字符串是不存在的全局常量，转化成他们自身的字符串。
在以前，该行为会产生 **`E_NOTICE`**，但现在会产生
**`E_WARNING`**。在下一个 PHP 主版本中，将抛出 <span
class="classname">Error</span> 异常。

``` php
<?php

var_dump(NONEXISTENT);

/* Output:
Warning: Use of undefined constant NONEXISTENT - assumed 'NONEXISTENT' (this will throw an Error in a future version of PHP) in %s on line %d
string(11) "NONEXISTENT"
*/
```

### <span class="function">png2wbmp</span> 和 <span class="function">jpeg2wbmp</span>

GD 扩展内的 <span class="function">png2wbmp</span> 和 <span
class="function">jpeg2wbmp</span> 现已被废弃，将在下一个 PHP
主版本中移除。

### **`INTL_IDNA_VARIANT_2003`** 转化

Intl 扩展废弃了 **`INTL_IDNA_VARIANT_2003`** 转化，为<span
class="function">idn\_to\_ascii</span> 和 <span
class="function">idn\_to\_utf8</span> 的默认选项。 PHP 7.4
会把默认值设置为 **`INTL_IDNA_VARIANT_UTS46`**， 并在下一个 PHP
主版本中完全移除 **`INTL_IDNA_VARIANT_2003`**。

### <span class="function">\_\_autoload</span> 方法

<span class="function">\_\_autoload</span> 方法已被废弃， 因为和 <span
class="function">spl\_autoload\_register</span> 相比功能较差
(因为无法链式处理多个 autoloader)， 而且也无法在两种 autoloading
样式中配合使用。

### `track_errors` ini 设置和 *$php\_errormsg* 变量

当开启了 `track_errors` ini 设置，出现非致命错误时， 会在本地作用域创建
*$php\_errormsg* 变量。 由于提供了更好的方式： <span
class="function">error\_get\_last</span>
来获取此类错误信息，该功能被废弃。

### <span class="function">create\_function</span> 函数

考虑到此函数的安全隐患问题（它是 <span class="function">eval</span>
的瘦包装器），该过时的函数现在已被废弃。
更好的选择是<a href="/functions/anonymous.html" class="link">匿名函数</a>。

### `mbstring.func_overload` ini 设置

由于此设置会影响环境中的字符串系列函数，带来相互操作中的问题，它现在已被废弃。

### *(unset)* 类型强制转化

转化任意表达式为此类型，结果总是
**`NULL`**，所以这个多余的类型转化现在也就被废弃了。

### <span class="function">parse\_str</span> 不加第二个参数

使用 <span class="function">parse\_str</span>
时，不加第二个参数会导致查询字符串参数导入当前符号表。
考虑到安全隐患问题，不加第二个参数使用 <span
class="function">parse\_str</span> 的行为已被废弃。
此函数的第二个选项为必填项，它使查询字符串转为 Array。

### <span class="function">gmp\_random</span> 函数

此函数基于未知的、取决于平台的 limb
尺寸产生随机数。因此，该函数已被废弃。 使用更好的方式产生随机数： GMP
扩展中的 <span class="function">gmp\_random\_bits</span> 和 <span
class="function">gmp\_random\_range</span>。

### <span class="function">each</span> 函数

使用此函数遍历时，比普通的 *foreach* 更慢，
并且给新语法的变化带来实现问题。因此它被废弃了。

### <span class="function">assert</span> 一个字符串参数

<span class="function">assert</span> 字符串参数将要求它能被 <span
class="function">eval</span> 执行。
考虑到可能被执行远程代码，废弃了字符串的 <span
class="function">assert</span>，最好提供 bool 的表达式。

### 错误处理器内的 *$errcontext* 参数

*$errcontext* 参数包含了错误网站的所有本地变量。
考虑到它很少被用到，而且还会导致内部优化问题，它现在被废弃了。
代替用法：调试器应该自己取回错误站点的本地变量。

### <span class="function">read\_exif\_data</span> 函数

<span class="function">read\_exif\_data</span> 别名已被废弃 使用 <span
class="function">exif\_read\_data</span> 函数代替。
