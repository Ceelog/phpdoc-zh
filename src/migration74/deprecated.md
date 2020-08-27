PHP 7.4.x 废弃的功能
--------------------

### PHP 核心中废弃的功能

#### 没有显式括号的嵌套三元运算符

嵌套的三元操作中，必须明确使用显式括号来决定操作的顺序。以前，如果不使用括号，在大多数情况下，左关联性不会导致预期的行为。

``` php
<?php
1 ? 2 : 3 ? 4 : 5;   // deprecated
(1 ? 2 : 3) ? 4 : 5; // ok
1 ? 2 : (3 ? 4 : 5); // ok
?>
```

#### 大括号访问数组和字符串索引

使用大括号访问数组及字符串索引的方式已被废弃。请使用 *$var\[$idx\]*
的语法来替代 *$var{$idx}*。

#### (real) 类型和 <span class="function">is\_real</span> 函数

*(real)* 类型已被废弃，请使用 *(float)* 来替代。

同时被废弃的还有 <span class="function">is\_real</span> 函数，请使用
<span class="function">is\_float</span> 来替代。

#### Unbinding *$this* when *$this* is used

Unbinding *$this* of a non-static closure that uses *$this* is
deprecated.

#### *parent* 关键词在没父类的类中使用

在没有父类的类中使用 *parent* 关键词已被废弃，并且在将来的 PHP
版本中将会抛出一个编译错误。目前只在运行时访问父类时才会产生错误。

#### allow\_url\_include INI 选项

配置文件中的
<a href="/filesystem/setup.html#" class="link">allow_url_include</a>
选项被废弃。如果启用了该选项，将会产生一个弃用通知。

#### 基础转换函数中的无效字符处理

在下面这些基础转换函数中，<span class="function">base\_convert</span>,
<span class="function">bindec</span>, <span
class="function">octdec</span> 和 <span class="function">hexdec</span>
如果传入了非法字符，将会抛出一个弃用通知。函数会忽略掉无效字符后正常返回结果。前导空格和尾部空格，以及类型为
0x (取决于基数) 被允许传入。

#### 在对象中使用 <span class="function">array\_key\_exists</span>

在一个对象中使用 <span class="function">array\_key\_exists</span>
已被废弃。请使用 <span class="function">isset</span> 或 <span
class="function">property\_exists</span> 来替代。

#### 魔术引号函数

魔术引号函数 <span class="function">get\_magic\_quotes\_gpc</span> 和
<span class="function">get\_magic\_quotes\_runtime</span>
已被废弃。它们将永远返回 **`FALSE`**。

#### <span class="function">hebrevc</span> 函数

<span class="function">hebrevc</span> 函数已被废弃。 可以用
*nl2br(hebrev($str))* 来替代，更好的方法是启用 Unicode RTL 来支持。

#### <span class="function">convert\_cyr\_string</span> 函数

<span class="function">convert\_cyr\_string</span> 函数已被废弃。可以用
<span class="function">mb\_convert\_string</span>， <span
class="function">iconv</span> 或 <span
class="classname">UConverter</span> 替代。

#### <span class="function">money\_format</span> 函数

<span class="function">money\_format</span> 函数已被废弃。
可以用更国际化的 <span class="classname">NumberFormatter</span>
功能来替代。

#### <span class="function">ezmlm\_hash</span> 函数

<span class="function">ezmlm\_hash</span> 函数已被废弃。

#### <span class="function">restore\_include\_path</span> 函数

<span class="function">restore\_include\_path</span>
函数已被废弃。可以用 *ini\_restore('include\_path')* 替代。

#### Implode 函数的参数顺序

<span class="function">implode</span>
允许反转参数顺序的特性已被废弃，请使用 *implode($glue, $parts)* 来替代
*implode($parts, $glue)*。

### COM

导入类型库的大小写不敏感的常量注册已被废弃。

### Filter

**`FILTER_SANITIZE_MAGIC_QUOTES`** 已被废弃，使用
**`FILTER_SANITIZE_ADD_SLASHES`** 来替代。

### Multibyte String

Passing a non-string pattern to <span
class="function">mb\_ereg\_replace</span> is deprecated. Currently,
non-string patterns are interpreted as ASCII codepoints. In PHP 8, the
pattern will be interpreted as a string instead.

Passing the encoding as 3rd parameter to <span
class="function">mb\_strrpos</span> is deprecated. Instead pass a 0
offset, and encoding as 4th parameter.

### Lightweight Directory Access Protocol

<span class="function">ldap\_control\_paged\_result\_response</span> 和
<span class="function">ldap\_control\_paged\_result</span>
函数已被废弃。控制页面操作可以使用 <span
class="function">ldap\_search</span> 替代。

### Reflection

调用 <span class="methodname">ReflectionType::\_\_toString</span>
现在将会抛出一个弃用通知。 该方法从 PHP 7.1 开始，在 <span
class="methodname">ReflectionNamedType::getName</span>
的文档中已经被声明废弃，但是由于技术原因，并没有抛出弃用通知。

The *export()* methods on all <span class="classname">Reflection</span>
classes are deprecated. Construct a <span
class="classname">Reflection</span> object and convert it to string
instead:

``` php
<?php
// ReflectionClass::export(Foo::class, false) is:
echo new ReflectionClass(Foo::class), "\n";

// $str = ReflectionClass::export(Foo::class, true) is:
$str = (string) new ReflectionClass(Foo::class);
?>
```

### Socket

常量 **`AI_IDN_ALLOW_UNASSIGNED`** 和 **`AI_IDN_USE_STD3_ASCII_RULES`**
在 <span class="function">socket\_addrinfo\_lookup</span>
中不再可用，因为该常量在 glibc 中已被废弃。
