opcache\_compile\_file
======================

无需运行，即可编译并缓存 PHP 脚本

### 说明

<span class="type">boolean</span> <span
class="methodname">opcache\_compile\_file</span> ( <span
class="methodparam"><span class="type">string</span> `$file`</span> )

该函数可以用于在不用运行某个 PHP 脚本的情况下，编译该 PHP
脚本并将其添加到字节码缓存中去。 该函数可用于在 Web
服务器重启之后初始化缓存，以供后续请求调用。

### 参数

`file`  
被编译的 PHP 脚本的路径。

### 返回值

如果 `file` 被成功编译，则返回 **`TRUE`** 或者在失败时返回 **`FALSE`**。

### 错误／异常

如果文件（ `file` ）不能被载入或者不能被编译，则会生成一个
**`E_WARNING`** 级别的错误。 可以使用
<a href="/language/operators/errorcontrol.html" class="link">@</a>
来抑制该警告。

### 参见

-   <span class="function">opcache\_invalidate</span>

opcache\_get\_configuration
===========================

获取缓存的配置信息

### 说明

<span class="type">array</span> <span
class="methodname">opcache\_get\_configuration</span> ( <span
class="methodparam">void</span> )

该函数将返回缓存实例的配置信息。

### 返回值

返回一个数组，该数组里包含了缓存的初始化信息，黑名单和版本号。

### 错误／异常

在启用了 *opcache.restrict\_api*
的情况下，如果当前路径在禁止规则里，将会出现 E\_WARNING
；不会返回任何状态信息。

### 参见

-   <span class="function">opcache\_get\_status</span>

opcache\_get\_status
====================

获取缓存的状态信息

### 说明

<span class="type">array</span> <span
class="methodname">opcache\_get\_status</span> (\[ <span
class="methodparam"><span class="type">boolean</span>
`$get_scripts`<span class="initializer"> = **`TRUE`**</span></span> \] )

该函数将返回缓存实例的状态信息。

### 参数

`get_scripts`  
包含脚本的具体声明信息。

### 返回值

返回一个数组，该数组可能包含有脚本具体的声明信息。

### 错误／异常

在启用了 *opcache.restrict\_api*
的情况下，如果当前路径在禁止规则里，将会出现 E\_WARNING
；不会返回任何状态信息。

### 参见

-   <span class="function">opcache\_get\_configuration</span>

opcache\_invalidate
===================

废除脚本缓存

### 说明

<span class="type">boolean</span> <span
class="methodname">opcache\_invalidate</span> ( <span
class="methodparam"><span class="type">string</span> `$script`</span>
\[, <span class="methodparam"><span class="type">boolean</span>
`$force`<span class="initializer"> = **`FALSE`**</span></span> \] )

该函数的作用是使得指定脚本的字节码缓存失效。 如果 `force`
没有设置或者传入的是 **`FALSE`**，那么只有当脚本的修改时间
比对应字节码的时间更新，脚本的缓存才会失效。

### 参数

`script`  
缓存需要被作废对应的脚本路径

`force`  
如果该参数设置为**`TRUE`**，那么不管是否必要，该脚本的缓存都将被废除。

### 返回值

如果脚本的字节码缓存失效设置成功或者该脚本本来就没有缓存，则返回
**`TRUE`**；如果字节码缓存被禁用，则返回**`FALSE`**。

### 参见

-   <span class="function">opcache\_compile\_file</span>
-   <span class="function">opcache\_reset</span>

opcache\_is\_script\_cached
===========================

Tells whether a script is cached in OPCache

### 说明

<span class="type">bool</span> <span
class="methodname">opcache\_is\_script\_cached</span> ( <span
class="methodparam"><span class="type">string</span> `$filename`</span>
)

This function checks if a PHP script has been cached in OPCache. This
can be used to more easily detect the "warming" of the cache for a
particular script.

### 参数

`filename`  
The path to the PHP script to be checked.

### 返回值

Returns **`TRUE`** if `filename` is cached in OPCache, **`FALSE`**
otherwise.

### 参见

-   <span class="function">opcache\_compile\_file</span>

opcache\_reset
==============

重置字节码缓存的内容

### 说明

<span class="type">boolean</span> <span
class="methodname">opcache\_reset</span> ( <span
class="methodparam">void</span> )

该函数将重置整个字节码缓存。 在调用 <span
class="function">opcache\_reset</span>
之后，所有的脚本将会重新载入并且在下次被点击的时候重新解析。

### 参数

此函数没有参数。

### 返回值

如果字节码缓存被重置成功，则返回
**`TRUE`**；如果字节码缓存被禁用，则返回 **`FALSE`**。

### 参见

-   <span class="function">opcache\_invalidate</span>

**目录**

-   [opcache\_compile\_file](/ref/opcache.html#opcache_compile_file) —
    无需运行，即可编译并缓存 PHP 脚本
-   [opcache\_get\_configuration](/ref/opcache.html#opcache_get_configuration)
    — 获取缓存的配置信息
-   [opcache\_get\_status](/ref/opcache.html#opcache_get_status) —
    获取缓存的状态信息
-   [opcache\_invalidate](/ref/opcache.html#opcache_invalidate) —
    废除脚本缓存
-   [opcache\_is\_script\_cached](/ref/opcache.html#opcache_is_script_cached)
    — Tells whether a script is cached in OPCache
-   [opcache\_reset](/ref/opcache.html#opcache_reset) —
    重置字节码缓存的内容
