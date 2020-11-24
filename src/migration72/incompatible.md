不向下兼容的变更
----------------

### 防止 <span class="function">number\_format</span> 返回负零

之前版本中，<span class="function">number\_format</span> 有可能会返回
*-0*。虽然这是符合 IEEE 754
规范的，但是这样会导致可读性不好，新版本中会将这样的负数去掉。

``` php
<?php

var_dump(number_format(-0.01)); // 新版本输出 string(1) "0" 旧版本输出 string(2) "-0"
```

### 转换对象和数组中的数字键

将数组转换为对象，或将对象转换为数组时，数字键现在得到了更好的处理（无论是通过显式转换还是通过
<span class="function">settype</span> 函数）。

这意味着现在可以访问数组中的整数(或者说是字符串整数)键，这些键会映射到对象中：

``` php
<?php

// array to object
$arr = [0 => 1];
$obj = (object)$arr;
var_dump(
    $obj,
    $obj->{'0'}, // 新写法
    $obj->{0} // 新写法
);
```

以上例程会输出：

    object(stdClass)#1 (1) {
      ["0"]=>    // string key now, rather than integer key
      int(1)
    }
    int(1)
    int(1)

从对象转换成的数组中的整数（或者说是字符串整数）键现在也可以直接访问：

``` php
<?php

// object to array
$obj = new class {
    public function __construct()
    {
        $this->{0} = 1;
    }
};
$arr = (array)$obj;
var_dump(
    $arr,
    $arr[0], // 新写法
    $arr['0'] // 新写法
);
```

以上例程会输出：

    array(1) {
      [0]=>    // integer key now, rather than string key
      int(1)
    }
    int(1)
    int(1)

### <span class="function">get\_class</span> 函数不再接受 **`NULL`** 参数

之前版本中，传递 **`NULL`** 给 <span class="function">get\_class</span>
函数将返回当前类名。在新版本中，此行为会抛出一个 **`E_WARNING`**
错误。如果想实现与之前版本同样的效果，请不要传递任何参数进来。

### 计算非可数类型（non-countable）时发出警告

对非可数类型调用 <span class="function">count</span>（或 <span
class="function">sizeof</span>）函数，会抛出一个 **`E_WARNING`** 错误。

``` php
<?php

var_dump(
    count(null), // NULL is not countable
    count(1), // integers are not countable
    count('abc'), // strings are not countable
    count(new stdclass), // objects not implementing the Countable interface are not countable
    count([1,2]) // arrays are countable
);
```

以上例程会输出：

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d

    Warning: count(): Parameter must be an array or an object that implements Countable in %s on line %d
    int(0)
    int(1)
    int(1)
    int(1)
    int(2)

### ext/hash 从资源变成对象

As part of the long-term migration away from resources, the
<a href="/book/hash.html" class="link">Hash</a> extension has been
updated to use objects instead of resources. The change should be
seamless for PHP developers, except for where <span
class="function">is\_resource</span> checks have been made (which will
need updating to <span class="function">is\_object</span> instead).

### SSL/TLS 的默认选项的改进

下列默认选项被修改：

-   <span class="simpara"> *tls://* 默认为 TLSv1.0 or TLSv1.1 or TLSv1.2
    </span>
-   <span class="simpara"> *ssl://* 成为 *tls://* 的别名 </span>
-   <span class="simpara"> *STREAM\_CRYPTO\_METHOD\_TLS\_\** 常量默认为
    TLSv1.0 或 TLSv1.1 + TLSv1.2，替代之前的 TLSv1.0 </span>

### <span class="function">gettype</span> 在闭包资源中的返回值

之前版本中，如果在一个闭包资源中使用 <span
class="function">gettype</span> 会返回字符串 *"unknown
type"*，现在将会返回字符 *"resource (closed)"*。

### <span class="function">is\_object</span> 和 <span class="classname">\_\_PHP\_Incomplete\_Class</span>

之前版本中，对 <span class="classname">\_\_PHP\_Incomplete\_Class</span>
调用 <span class="function">is\_object</span> 函数会返回
**`FALSE`**，现在会返回 **`TRUE`**。

### 提升未定义常量的错误级别

调用未定义的常量，现在会抛出一个 **`E_WARNING`** 错误(之前版本中为
**`E_NOTICE`**)。在下一个 PHP 大版本中，将会抛出一个 <span
class="classname">Error</span> 错误。

### Windows 支持

官方支持的最低 Windows 版本为 Windows 7/Server 2008 R2。

### Checks on default property values of traits

Compatibility checks upon default trait property values will no longer
perform casting.

### *object* 保留字的变化

*object* 在之前的 PHP 7.0 版本
中被声明为软保留字（soft-reserved）。现在变更为强制保留字，禁止在任何类或接口中使用该名称。

### NetWare 支持

NetWare 已不再被支持。

### <span class="function">array\_unique</span> with **`SORT_STRING`**

While <span class="function">array\_unique</span> with **`SORT_STRING`**
formerly copied the array and removed non-unique elements (without
packing the array afterwards), now a new array is built by adding the
unique elements. This can result in different numeric indexes.

### <span class="function">bcmod</span> changes with floats

The <span class="function">bcmod</span> function no longer truncates
fractional numbers to integers. As such, its behavior now follows <span
class="function">fmod</span>, rather than the *%* operator. For example
*bcmod('4', '3.5')* now returns *0.5* instead of *1*.

### Hashing functions and non-cryptographic hashes

The <span class="function">hash\_hmac</span>, <span
class="function">hash\_hmac\_file</span>, <span
class="function">hash\_pbkdf2</span>, and <span
class="function">hash\_init</span> (with **`HASH_HMAC`**) functions no
longer accept non-cryptographic hashes.

### <span class="function">json\_decode</span> 函数变更

The <span class="function">json\_decode</span> function option,
**`JSON_OBJECT_AS_ARRAY`**, is now used if the second parameter (assoc)
is **`NULL`**. Previously, **`JSON_OBJECT_AS_ARRAY`** was always
ignored.

### <span class="function">rand</span> and <span class="function">mt\_rand</span> output

Sequences generated by <span class="function">rand</span> and <span
class="function">mt\_rand</span> for a specific seed may differ from PHP
7.1 on 64-bit machines (due to the fixing of a modulo bias bug in the
implementation).

### <a href="/ini/core.html#ini.sql.safe-mode" class="link"><code class="parameter">sql.safe_mode</code></a> ini 选项移除

`sql.safe_mode` ini 设置项已被移除。

### Changes to <span class="function">date\_parse</span> and <span class="function">date\_parse\_from\_format</span>

The *zone* element of the array returned by <span
class="function">date\_parse</span> and <span
class="function">date\_parse\_from\_format</span> represents seconds
instead of minutes now, and its sign is inverted. For instance *-120* is
now *7200*.

### Incoming Cookies

As of PHP 7.2.34, the *names* of incoming cookies are no longer
url-decoded for security reasons.
