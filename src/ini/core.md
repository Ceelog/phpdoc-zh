`php.ini` 核心配置选项说明
--------------------------

该列表只包含核心的 `php.ini`
配置选项。扩展的配置选项在各个扩展的文档页面分别被描述。比如，有关
session 的选项可以在
<a href="/session/setup.html#运行时配置" class="link">sessions 页面</a>找到。

> **Note**:
>
> 以下列出了未设置 `php.ini` 时的默认值；开发环境和生产环境的 `php.ini`
> 值可能会有所不同。

语言选项
--------

| 名字                                                                                                        | 默认 | 可修改范围              | 更新日志                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------|------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <a href="/ini/core.html#ini.short-open-tag" class="link">short_open_tag</a>                                 | "1"  | PHP\_INI\_PERDIR        |                                                                                                                                   |
| <a href="/ini/core.html#ini.asp-tags" class="link">asp_tags</a>                                             | "0"  | PHP\_INI\_PERDIR        | PHP 7.0.0. 中移除。                                                                                                               |
| <a href="/ini/core.html#ini.precision" class="link">precision</a>                                           | "14" | PHP\_INI\_ALL           |                                                                                                                                   |
| <a href="/ini/core.html#ini.serialize-precision" class="link">serialize_precision</a>                       | "17" | PHP\_INI\_ALL           | 在 PHP 5.3.5以前，默认值为 100 在 PHP 7.1.0以前，默认值为 17                                                                      |
| <a href="/ini/core.html#ini.y2k-compliance" class="link">y2k_compliance</a>                                 | "1"  | PHP\_INI\_ALL           | 在 PHP 5.4.0 中移除该选项。                                                                                                       |
| <a href="/ini/core.html#ini.allow-call-time-pass-reference" class="link">allow_call_time_pass_reference</a> | "1"  | PHP\_INI\_PERDIR        | 在 PHP 5.4.0 中移除该选项。                                                                                                       |
| <a href="/ini/core.html#ini.disable-functions" class="link">disable_functions</a>                           | ""   | 仅仅为 PHP\_INI\_SYSTEM |                                                                                                                                   |
| <a href="/ini/core.html#ini.disable-classes" class="link">disable_classes</a>                               | ""   | 仅仅为 `php.ini`        |                                                                                                                                   |
| <a href="/ini/core.html#ini.exit-on-timeout" class="link">exit_on_timeout</a>                               | ""   | PHP\_INI\_ALL           | 从 PHP 5.3.0 起可用。                                                                                                             |
| <a href="/ini/core.html#ini.expose-php" class="link">expose_php</a>                                         | "1"  | `php.ini` only          |                                                                                                                                   |
| <a href="/ini/core.html#ini.hard-timeout" class="link">hard_timeout</a>                                     | "2"  | PHP\_INI\_SYSTEM        | PHP 7.1.0 起可用                                                                                                                  |
| <a href="/ini/core.html#ini.zend.exception-ignore-args" class="link">zend.exception_ignore_args</a>         | "0"  | PHP\_INI\_ALL           | PHP 7.4.0 起可用                                                                                                                  |
| <a href="/ini/core.html#ini.zend.multibyte" class="link">zend.multibyte</a>                                 | "0"  | PHP\_INI\_ALL           | 从 PHP 5.4.0 起可用                                                                                                               |
| <a href="/ini/core.html#ini.zend.script-encoding" class="link">zend.script_encoding</a>                     | NULL | PHP\_INI\_ALL           | 从 PHP 5.4.0 起可用                                                                                                               |
| <a href="/ini/core.html#ini.zend.detect-unicode" class="link">zend.detect-unicode</a>                       | NULL | PHP\_INI\_ALL           | 从 PHP 5.4.0 起可用                                                                                                               |
| <a href="/ini/core.html#ini.zend.signal-check" class="link">zend.signal_check</a>                           | "0"  | PHP\_INI\_SYSTEM        | 从 PHP 5.4.0 起可用                                                                                                               |
| <a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>                               | "1"  | PHP\_INI\_ALL           | 从 PHP 7.0.0 起可用                                                                                                               |
| <a href="/ini/core.html#ini.zend.ze1-compatibility-mode" class="link">zend.ze1_compatibility_mode</a>       | "0"  | PHP\_INI\_ALL           | 在 PHP 5.3.0 中移除该选项                                                                                                         |
| detect\_unicode                                                                                             | "1"  | PHP\_INI\_ALL           | 从 PHP 5.1.0起可用。 PHP 5.4.0 起重命名为 <a href="/ini/core.html#ini.zend.detect-unicode" class="link">zend.detect-unicode</a>。 |

这是配置指令的简短说明。

`short_open_tag` <span class="type">boolean</span>  
决定是否允许使用 PHP
代码开始标志的缩写形式（**`<?          ?>`**）。如果要和 XML 结合使用
PHP，可以禁用此选项以便于嵌入使用 **`<?xml ?>`**。否则还可以通过 PHP
来输出，例如：**`<?php echo '<?xml          version="1.0"'; ?>`**。如果禁用了，必须使用
PHP 代码开始标志的完整形式（**`<?php          ?>`**）。

> **Note**:
>
> 本指令也会影响到缩写形式 **`<?=`**，它和 **`<? echo`**
> 等价。使用此缩写需要 `short_open_tag` 的值为 On。 从 PHP 5.4.0 起，
> **`<?=`** 总是可用的。

`asp_tags` <span class="type">boolean</span>  
<span class="simpara"> 除了通常的 \<?php ?\> 标志之外还允许使用 ASP
风格的标志 \<% %\>。这也包括了输出变量值的缩写 \<%= $value
%\>。更多信息见<a href="/language/basic-syntax/phpmode.html" class="link">从 HTML 中分离</a>一节。
</span>

| 版本  | 说明            |
|-------|-----------------|
| 7.0.0 | 从 PHP 中移除。 |

`precision` <span class="type">integer</span>  
<span class="simpara"> 浮点数中显示有效数字的位数。*-1* means that an
enhanced algorithm for rounding such numbers will be used. </span>

`serialize_precision` <span class="type">integer</span>  
<span class="simpara"> The number of significant digits stored while
serializing floating point numbers. *-1* means that an enhanced
algorithm for rounding such numbers will be used. </span>

`y2k_compliance` <span class="type">boolean</span>  
<span class="simpara"> 强制 2000 年兼容（在不兼容的浏览器中会出问题）。
</span>

`allow_call_time_pass_reference` <span class="type">boolean</span>  
在函数调用时参数被按照引用传递时是否发出警告。此方法已不被赞成并在
PHP/Zend
未来的版本中很可能不再支持。鼓励使用的方法是在函数定义中指定哪些参数应该用引用传递。鼓励大家尝试关闭此选项并确保脚本能够正常运行，以确保该脚本也能在未来的版本中运行（每次使用此特性都会收到一条警告）。

在函数调用时通过引用传递参数是不推荐的，因为它影响到了代码的整洁。如果函数的参数没有声明作为引用传递，函数可以通过未写入文档的方法修改其参数。要避免其副作用，最好仅在函数声明时指定那个参数需要通过引用传递。

参见<a href="/language/references.html" class="link">引用的解释</a>。

| 版本  | 说明                                                              |
|-------|-------------------------------------------------------------------|
| 5.4.0 | 从 PHP 中移除。                                                   |
| 5.3.0 | Emits an **`E_DEPRECATED`** level error.                          |
| 5.0.0 | Deprecated, and generates an **`E_COMPILE_WARNING`** level error. |

`expose_php` <span class="type">boolean</span>  
决定是否暴露 PHP 被安装在服务器上（例如在 Web
服务器的信息头中加上其签名：X-Powered-By: PHP/5.3.7)。 The PHP logo
guids are also exposed, thus appending them to the URL of a PHP enabled
site will display the appropriate logo (e.g.,
<a href="https://www.php.net/?=PHPE9568F34-D428-11d2-A769-00AA001ACF42" class="link external">» https://www.php.net/?=PHPE9568F34-D428-11d2-A769-00AA001ACF42</a>).
This also affects the output of <span class="function">phpinfo</span>,
as when disabled, the PHP logo and credits information will not be
displayed.

> **Note**:
>
> Since PHP 5.5.0 these guids and the <span
> class="function">php\_logo\_guid</span> function have been removed
> from PHP and the guids are replaced with data URIs instead. Thus
> accessing the PHP logo via appending the guid to the URL no longer
> works. Similarly, turning `expose_php` off will not affect seeing the
> PHP logo in <span class="function">phpinfo</span>.

See also <span class="function">php\_logo\_guid</span> and <span
class="function">phpcredits</span>.

`disable_functions` <span class="type">string</span>  
本指令可用于禁止某些函数。接受逗号分隔的函数名列表作为参数。

此指令仅能禁用
<a href="/functions/internal.html" class="link">内置函数</a>。
不能影响<a href="/functions/user-defined.html" class="link">用户自定义函数</a>。

本指令只能设置在 `php.ini` 中。例如，无法在 `httpd.conf` 中设置。

`disable_classes` <span class="type">string</span>  
<span class="simpara"> 本指令可以使你禁用某些类。用逗号分隔类名。
</span> <span class="simpara"> 本指令只能设置在 `php.ini`
中。例如不能将其设置在 `httpd.conf`。 </span>

`zend.assertions` <span class="type">integer</span>  
<span class="simpara"> When set to *1*, assertion code will be generated
and executed (development mode). When set to *0*, assertion code will be
generated but it will be skipped (not executed) at runtime. When set to
*-1*, assertion code will not be generated, making the assetions
zero-cost (production mode). </span>

> **Note**:
>
> If a process is started in production mode,
> <a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
> cannot be changed at runtime, since the code for assertions was not
> generated.
>
> If a process is started in development mode,
> <a href="/ini/core.html#ini.zend.assertions" class="link">zend.assertions</a>
> cannot be set to *-1* at runtime.

`zend.ze1_compatibility_mode` <span class="type">boolean</span>  
Enable compatibility mode with Zend Engine 1 (PHP 4). It affects the
cloning, casting (objects with no properties cast to **`FALSE`** or 0),
and
<a href="/language/oop5/object-comparison.html" class="link">comparing of objects</a>.
In this mode, objects are passed by value instead of reference by
default.

See also the section titled
<a href="/migration5.html" class="link">Migrating from PHP 4 to PHP 5</a>.

**Warning**
This feature has been *DEPRECATED* and *REMOVED* as of PHP 5.3.0.

`hard_timeout` <span class="type">integer</span>  

`zend.exception_ignore_args` <span class="type">boolean</span>  
Excludes arguments from stack traces generated from exceptions.

`zend.multibyte` <span class="type">boolean</span>  
Enables parsing of source files in multibyte encodings. Enabling
zend.multibyte is required to use character encodings like SJIS, BIG5,
etc that contain special characters in multibyte string data. ISO-8859-1
compatible encodings like UTF-8, EUC, etc do not require this option.

Enabling zend.multibyte requires the mbstring extension to be available.

`zend.script_encoding` <span class="type">string</span>  
This value will be used unless a
<a href="/control-structures/declare.html#control-structures.declare.encoding" class="link">declare(encoding=...)</a>
directive appears at the top of the script. When ISO-8859-1 incompatible
encoding is used, both zend.multibyte and zend.script\_encoding must be
used.

Literal strings will be transliterated from zend.script\_enconding to
mbstring.internal\_encoding, as if <span
class="function">mb\_convert\_encoding</span> would have been called.

`zend.detect_unicode` <span class="type">boolean</span>  
Check for BOM (Byte Order Mark) and see if the file contains valid
multibyte characters. This detection is performed before processing of
<span class="function">\_\_halt\_compiler</span>. Available only in Zend
Multibyte mode.

`zend.signal_check` <span class="type">boolean</span>  
To check for replaced signal handlers on shutdown.

`exit_on_timeout` <span class="type">boolean</span>  
This is an Apache1 mod\_php-only directive that forces an Apache child
to exit if a PHP execution timeout occurred. Such a timeout causes an
internal longjmp() call in Apache1 which can leave some extensions in an
inconsistent state. By terminating the process any outstanding locks or
memory will be cleaned up.

Resource Limits
---------------

| 名字                                                                    | 默认   | 可修改范围    | 更新日志                                  |
|-------------------------------------------------------------------------|--------|---------------|-------------------------------------------|
| <a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a> | "128M" | PHP\_INI\_ALL | "8M" before PHP 5.2.0, "16M" in PHP 5.2.0 |

这是配置指令的简短说明。

`memory_limit` <span class="type">integer</span>  
This sets the maximum amount of memory in bytes that a script is allowed
to allocate. This helps prevent poorly written scripts for eating up all
available memory on a server. Note that to have no memory limit, set
this directive to *-1*.

Prior to PHP 5.2.1, in order to use this directive it had to be enabled
at compile time by using **--enable-memory-limit** in the configure
line. This compile-time flag was also required to define the functions
<span class="function">memory\_get\_usage</span> and <span
class="function">memory\_get\_peak\_usage</span> prior to 5.2.1.

<span class="simpara">当使用 <span class="type">integer</span> 时,
其值以字节来衡量。还可以使用在<a href="/faq/using.html#faq.using.shorthandbytes" class="link">FAQ</a>中描述的速记符。</span>

See also:
<a href="/info/setup.html#" class="link">max_execution_time</a>.

Performance Tuning
------------------

| 名字                                                                                  | 默认  | 可修改范围       | 更新日志                                                                          |
|---------------------------------------------------------------------------------------|-------|------------------|-----------------------------------------------------------------------------------|
| <a href="/ini/core.html#ini.realpath-cache-size" class="link">realpath_cache_size</a> | "4M"  | PHP\_INI\_SYSTEM | Available since PHP 5.1.0. Prior to PHP 7.0.16 and 7.1.2, the default was *"16K"* |
| <a href="/ini/core.html#ini.realpath-cache-ttl" class="link">realpath_cache_ttl</a>   | "120" | PHP\_INI\_SYSTEM | Available since PHP 5.1.0.                                                        |

> **Note**:
>
> Using
> <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
> will *disable* the realpath cache.

这是配置指令的简短说明。

`realpath_cache_size` <span class="type">integer</span>  
Determines the size of the realpath cache to be used by PHP. This value
should be increased on systems where PHP opens many files, to reflect
the quantity of the file operations performed.

The size represents the total number of bytes in the path strings
stored, plus the size of the data associated with the cache entry. This
means that in order to store longer paths in the cache, the cache size
must be larger. This value does not directly control the number of
distinct paths that can be cached.

The size required for the cache entry data is system dependent.

`realpath_cache_ttl` <span class="type">integer</span>  
Duration of time (in seconds) for which to cache realpath information
for a given file or directory. For systems with rarely changing files,
consider increasing the value.

Data Handling
-------------

| 名字                                                                                                      | 默认        | 可修改范围       | 更新日志                                                         |
|-----------------------------------------------------------------------------------------------------------|-------------|------------------|------------------------------------------------------------------|
| <a href="/ini/core.html#ini.arg-separator.output" class="link">arg_separator.output</a>                   | "&"         | PHP\_INI\_ALL    |                                                                  |
| <a href="/ini/core.html#ini.arg-separator.input" class="link">arg_separator.input</a>                     | "&"         | PHP\_INI\_PERDIR |                                                                  |
| <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>                             | "EGPCS"     | PHP\_INI\_PERDIR | PHP\_INI\_ALL in PHP \<= 5.0.5.                                  |
| <a href="/ini/core.html#ini.request-order" class="link">request_order</a>                                 | ""          | PHP\_INI\_PERDIR | Available since PHP 5.3.0                                        |
| <a href="/ini/core.html#ini.auto-globals-jit" class="link">auto_globals_jit</a>                           | "1"         | PHP\_INI\_PERDIR | Available since PHP 5.0.0.                                       |
| <a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>                           | "0"         | PHP\_INI\_PERDIR | Removed in PHP 5.4.0.                                            |
| <a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>                       | "1"         | PHP\_INI\_PERDIR |                                                                  |
| <a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>                   | "1"         | PHP\_INI\_PERDIR | Deprecated in PHP 5.3.0. Removed in PHP 5.4.0.                   |
| <a href="/ini/core.html#ini.enable-post-data-reading" class="link">enable_post_data_reading</a>           | "1"         | PHP\_INI\_PERDIR | Available since PHP 5.4.0                                        |
| <a href="/ini/core.html#ini.post-max-size" class="link">post_max_size</a>                                 | "8M"        | PHP\_INI\_PERDIR |                                                                  |
| <a href="/ini/core.html#ini.auto-prepend-file" class="link">auto_prepend_file</a>                         | NULL        | PHP\_INI\_PERDIR |                                                                  |
| <a href="/ini/core.html#ini.auto-append-file" class="link">auto_append_file</a>                           | NULL        | PHP\_INI\_PERDIR |                                                                  |
| <a href="/ini/core.html#ini.default-mimetype" class="link">default_mimetype</a>                           | "text/html" | PHP\_INI\_ALL    |                                                                  |
| <a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>                             | "UTF-8"     | PHP\_INI\_ALL    | Defaults to "UTF-8" since PHP \>= 5.6.0; empty for PHP \< 5.6.0. |
| <a href="/ini/core.html#ini.always-populate-raw-post-data" class="link">always_populate_raw_post_data</a> | "0"         | PHP\_INI\_PERDIR | Removed in PHP 7.0.0.                                            |

这是配置指令的简短说明。

`arg_separator.output` <span class="type">string</span>  
The separator used in PHP generated URLs to separate arguments.

`arg_separator.input` <span class="type">string</span>  
List of separator(s) used by PHP to parse input URLs into variables.

> **Note**:
>
> Every character in this directive is considered as separator!

`variables_order` <span class="type">string</span>  
Sets the order of the EGPCS (*E*nvironment, *G*et, *P*ost, *C*ookie, and
*S*erver) variable parsing. For example, if variables\_order is set to
*"SP"* then PHP will create the
<a href="/language/variables/predefined.html" class="link">superglobals</a>
`$_SERVER` and `$_POST`, but not create `$_ENV`, `$_GET`, and
`$_COOKIE`. Setting to "" means no
<a href="/language/variables/predefined.html" class="link">superglobals</a>
will be set.

If the deprecated
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>
directive is on, then variables\_order also configures the order the
*ENV*, *GET*, *POST*, *COOKIE* and *SERVER* variables are populated in
global scope. So for example if variables\_order is set to *"EGPCS"*,
register\_globals is enabled, and both `$_GET['action']` and
`$_POST['action']` are set, then `$action` will contain the value of
`$_POST['action']` as *P* comes after *G* in our example directive
value.

**Warning**
In both the CGI and FastCGI SAPIs, `$_SERVER` is also populated by
values from the environment; *S* is always equivalent to *ES* regardless
of the placement of *E* elsewhere in this directive.

> **Note**:
>
> The content and order of `$_REQUEST` is also affected by this
> directive.

`request_order` <span class="type">string</span>  
This directive describes the order in which PHP registers GET, POST and
Cookie variables into the \_REQUEST array. Registration is done from
left to right, newer values override older values.

If this directive is not set,
<a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
is used for `$_REQUEST` contents.

Note that the default distribution `php.ini` files does not contain the
*'C'* for cookies, due to security concerns.

`auto_globals_jit` <span class="type">boolean</span>  
When enabled, the SERVER, REQUEST, and ENV variables are created when
they're first used (Just In Time) instead of when the script starts. If
these variables are not used within a script, having this directive on
will result in a performance gain.

The PHP directives
<a href="/ini/core.html#ini.register-globals" class="link">register_globals</a>,
<a href="/ini/core.html#ini.register-long-arrays" class="link">register_long_arrays</a>,
and
<a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>
must be disabled for this directive to have any affect. Since PHP 5.1.3
it is not necessary to have
<a href="/ini/core.html#ini.register-argc-argv" class="link">register_argc_argv</a>
disabled.

**Warning**
Usage of SERVER, REQUEST, and ENV variables is checked during the
compile time so using them through e.g.
<a href="/language/variables/variable.html" class="link">variable variables</a>
will not cause their initialization.

`register_globals` <span class="type">boolean</span>  
Whether or not to register the EGPCS (Environment, GET, POST, Cookie,
Server) variables as global variables.

As of
<a href="https://www.php.net/releases/4_2_0.php" class="link external">» PHP 4.2.0</a>,
this directive defaults to *off*.

Please read the security chapter on
<a href="/security/globals.html" class="link">Using register_globals</a>
for related information.

Please note that `register_globals` cannot be set at runtime (<span
class="function">ini\_set</span>). Although, you can use `.htaccess` if
your host allows it as described above. An example `.htaccess` entry:
**`php_flag register_globals off`**.

> **Note**:
>
> `register_globals` is affected by the
> <a href="/ini/core.html#ini.variables-order" class="link">variables_order</a>
> directive.

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

`register_argc_argv` <span class="type">boolean</span>  
<span class="simpara"> Tells PHP whether to declare the argv & argc
variables (that would contain the GET information). </span> <span
class="simpara"> See also
<a href="/features/commandline.html" class="link">command line</a>.
</span>

`register_long_arrays` <span class="type">boolean</span>  
<span class="simpara"> Tells PHP whether or not to register the
deprecated long `$HTTP_*_VARS` type
<a href="/language/variables/predefined.html" class="link">predefined variables</a>.
When On (default), long predefined PHP variables like `$HTTP_GET_VARS`
will be defined. If you're not using them, it's recommended to turn them
off, for performance reasons. Instead, use the superglobal arrays, like
`$_GET`. </span> <span class="simpara"> This directive became available
in PHP 5.0.0. </span>

**Warning**
本特性已自 PHP 5.3.0 起*废弃*并将自 PHP 5.4.0 起*移除*。

`enable_post_data_reading` <span class="type">boolean</span>  
<span class="simpara"> Disabling this option causes `$_POST` and
`$_FILES` *not* to be populated. The only way to read postdata will then
be through the <a href="/wrappers/php.html" class="link">php://input</a>
stream wrapper. This can be useful to proxy requests or to process the
POST data in a memory efficient fashion. </span>

`post_max_size` <span class="type">integer</span>  
<span class="simpara"> Sets max size of post data allowed. This setting
also affects file upload. To upload large files, this value must be
larger than
<a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>.
</span> <span class="simpara"> Generally speaking,
<a href="/ini/core.html#ini.memory-limit" class="link">memory_limit</a>
should be larger than `post_max_size`. </span> <span
class="simpara">当使用 <span class="type">integer</span> 时,
其值以字节来衡量。还可以使用在<a href="/faq/using.html#faq.using.shorthandbytes" class="link">FAQ</a>中描述的速记符。</span>
<span class="simpara"> If the size of post data is greater than
post\_max\_size, the `$_POST` and `$_FILES`
<a href="/language/variables/superglobals.html" class="link">superglobals</a>
are empty. This can be tracked in various ways, e.g. by passing the
`$_GET` variable to the script processing the data, i.e. *\<form
action="edit.php?processed=1"\>*, and then checking if
`$_GET['processed']` is set. </span>

> **Note**:
>
> PHP allows shortcuts for byte values, including K (kilo), M (mega) and
> G (giga). PHP will do the conversions automatically if you use any of
> these. Be careful not to exceed the 32 bit signed integer limit (if
> you're using 32bit versions) as it will cause your script to fail.

| 版本           | 说明                                                                                                                                     |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 5.3.4          | `post_max_size` = 0 will not disable the limit when the content type is application/x-www-form-urlencoded or is not registered with PHP. |
| 5.3.2 , 5.2.12 | Allow unlimited post size by setting `post_max_size` to 0.                                                                               |

`auto_prepend_file` <span class="type">string</span>  
Specifies the name of a file that is automatically parsed before the
main file. The file is included as if it was called with the <span
class="function">require</span> function, so
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
is used.

The special value *none* disables auto-prepending.

`auto_append_file` <span class="type">string</span>  
Specifies the name of a file that is automatically parsed after the main
file. The file is included as if it was called with the <span
class="function">require</span> function, so
<a href="/ini/core.html#ini.include-path" class="link">include_path</a>
is used.

The special value *none* disables auto-appending.

> **Note**: <span class="simpara"> If the script is terminated with
> <span class="function">exit</span>, auto-append will *not*
> occur.</span>

`default_mimetype` <span class="type">string</span>  
By default, PHP will output a media type using the Content-Type header.
To disable this, simply set it to be empty.

PHP's built-in default media type is set to text/html.

`default_charset` <span class="type">string</span>  
In PHP 5.6 onwards, "UTF-8" is the default value and its value is used
as the default character encoding for <span
class="function">htmlentities</span>, <span
class="function">html\_entity\_decode</span> and <span
class="function">htmlspecialchars</span> if the `encoding` parameter is
omitted. The value of `default_charset` will also be used to set the
default character set for
<a href="/book/iconv.html" class="link">iconv</a> functions if the
<a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.input_encoding</code></a>,
<a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.output_encoding</code></a>
and
<a href="/iconv/setup.html#" class="link"><code class="parameter">iconv.internal_encoding</code></a>
configuration options are unset, and for
<a href="/book/mbstring.html" class="link">mbstring</a> functions if the
<a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.http_input</code></a>
<a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.http_output</code></a>
<a href="/mbstring/setup.html#" class="link"><code class="parameter">mbstring.internal_encoding</code></a>
configuration option is unset.

All versions of PHP will use this value as the charset within the
default Content-Type header sent by PHP if the header isn't overridden
by a call to <span class="function">header</span>.

Setting `default_charset` to an empty value is not recommended.

`input_encoding` <span class="type">string</span>  
Available from PHP 5.6.0. This setting is used for multibyte modules
such as mbstring and iconv. Default is empty.

`output_encoding` <span class="type">string</span>  
Available from PHP 5.6.0. This setting is used for multibyte modules
such as mbstring and iconv. Default is empty.

`internal_encoding` <span class="type">string</span>  
Available from PHP 5.6.0. This setting is used for multibyte modules
such as mbstring and iconv. Default is empty. If empty,
<a href="/ini/core.html#ini.default-charset" class="link">default_charset</a>
is used.

`always_populate_raw_post_data` <span class="type">mixed</span>  
**Warning**
This feature was *DEPRECATED* in PHP 5.6.0, and *REMOVED* as of PHP
7.0.0.

If set to **`TRUE`**, PHP will always populate the `$HTTP_RAW_POST_DATA`
containing the raw POST data. Otherwise, the variable is populated only
when the MIME type of the data is unrecognised.

The preferred method for accessing raw POST data is
<a href="/wrappers/php.html" class="link">php://input</a>, and
`$HTTP_RAW_POST_DATA` is deprecated in PHP 5.6.0 onwards. Setting
`always_populate_raw_post_data` to *-1* will opt into the new behaviour
that will be implemented in a future version of PHP, in which
`$HTTP_RAW_POST_DATA` is never defined.

Regardless of the setting, `$HTTP_RAW_POST_DATA` is not available with
*enctype="multipart/form-data"*.

See also: <a href="/info/setup.html#" class="link">magic_quotes_gpc</a>,
<a href="/info/setup.html#" class="link">magic_quotes_runtime</a>, and
<a href="/book/sybase.html#" class="link">magic_quotes_sybase</a>.

Paths and Directories
---------------------

| 名字                                                                                          | 默认                  | 可修改范围       | 更新日志                          |
|-----------------------------------------------------------------------------------------------|-----------------------|------------------|-----------------------------------|
| <a href="/ini/core.html#ini.include-path" class="link">include_path</a>                       | ".;/path/to/php/pear" | PHP\_INI\_ALL    |                                   |
| <a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>                       | NULL                  | PHP\_INI\_ALL    | PHP\_INI\_SYSTEM in PHP \< 5.3.0  |
| <a href="/ini/core.html#ini.doc-root" class="link">doc_root</a>                               | NULL                  | PHP\_INI\_SYSTEM |                                   |
| <a href="/ini/core.html#ini.user-dir" class="link">user_dir</a>                               | NULL                  | PHP\_INI\_SYSTEM |                                   |
| <a href="/ini/core.html#ini.user-ini.cache-ttl" class="link">user_ini.cache_ttl</a>           | "300"                 | PHP\_INI\_SYSTEM | Available since PHP 5.3.0.        |
| <a href="/ini/core.html#ini.user-ini.filename" class="link">user_ini.filename</a>             | ".user.ini"           | PHP\_INI\_SYSTEM | Available since PHP 5.3.0.        |
| <a href="/ini/core.html#ini.extension-dir" class="link">extension_dir</a>                     | "/path/to/php"        | PHP\_INI\_SYSTEM |                                   |
| <a href="/ini/core.html#ini.extension" class="link">extension</a>                             | NULL                  | `php.ini` only   |                                   |
| <a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>                   | NULL                  | `php.ini` only   |                                   |
| <a href="/ini/core.html#ini.zend-extension-debug" class="link">zend_extension_debug</a>       | NULL                  | `php.ini` only   | Available before PHP 5.3.0.       |
| <a href="/ini/core.html#ini.zend-extension-debug-ts" class="link">zend_extension_debug_ts</a> | NULL                  | `php.ini` only   | Available before PHP 5.3.0.       |
| <a href="/ini/core.html#ini.zend-extension-ts" class="link">zend_extension_ts</a>             | NULL                  | `php.ini` only   | Available before PHP 5.3.0.       |
| <a href="/ini/core.html#ini.cgi.check-shebang-line" class="link">cgi.check_shebang_line</a>   | "1"                   | PHP\_INI\_SYSTEM | Available since PHP 5.2.0.        |
| <a href="/ini/core.html#ini.cgi.discard-path" class="link">cgi.discard_path</a>               | "0"                   | PHP\_INI\_SYSTEM | Available since PHP 5.3.0.        |
| <a href="/ini/core.html#ini.cgi.fix-pathinfo" class="link">cgi.fix_pathinfo</a>               | "1"                   | PHP\_INI\_SYSTEM | PHP\_INI\_ALL prior to PHP 5.2.1. |
| <a href="/ini/core.html#ini.cgi.force-redirect" class="link">cgi.force_redirect</a>           | "1"                   | PHP\_INI\_SYSTEM | PHP\_INI\_ALL prior to PHP 5.2.1. |
| <a href="/ini/core.html#ini.cgi.nph" class="link">cgi.nph</a>                                 | "0"                   | PHP\_INI\_SYSTEM | Available since PHP 5.3.0.        |
| <a href="/ini/core.html#ini.cgi.redirect-status-env" class="link">cgi.redirect_status_env</a> | NULL                  | PHP\_INI\_SYSTEM | PHP\_INI\_ALL prior to PHP 5.2.1. |
| <a href="/ini/core.html#ini.cgi.rfc2616-headers" class="link">cgi.rfc2616_headers</a>         | "0"                   | PHP\_INI\_ALL    |                                   |
| <a href="/ini/core.html#ini.fastcgi.impersonate" class="link">fastcgi.impersonate</a>         | "0"                   | PHP\_INI\_SYSTEM | PHP\_INI\_ALL prior to PHP 5.2.1. |
| <a href="/ini/core.html#ini.fastcgi.logging" class="link">fastcgi.logging</a>                 | "1"                   | PHP\_INI\_SYSTEM | PHP\_INI\_ALL prior to PHP 5.2.1. |

这是配置指令的简短说明。

`include_path` <span class="type">string</span>  
Specifies a list of directories where the <span
class="function">require</span>, <span class="function">include</span>,
<span class="function">fopen</span>, <span class="function">file</span>,
<span class="function">readfile</span> and <span
class="function">file\_get\_contents</span> functions look for files.
The format is like the system's `PATH` environment variable: a list of
directories separated with a colon in Unix or semicolon in Windows.

PHP considers each entry in the include path separately when looking for
files to include. It will check the first path, and if it doesn't find
it, check the next path, until it either locates the included file or
returns with an **`E_WARNING`** or an **`E_ERROR`**. You may modify or
set your include path at runtime using <span
class="function">set\_include\_path</span>.

**示例 \#1 Unix include\_path**

``` php.ini
include_path=".:/php/includes"
```

**示例 \#2 Windows include\_path**

``` php.ini
include_path=".;c:\php\includes"
```

Using a *.* in the include path allows for relative includes as it means
the current directory. However, it is more efficient to explicitly use
*include './file'* than having PHP always check the current directory
for every include.

> **Note**:
>
> *ENV* variables are also accessible in .ini files. As such it is
> possible to reference the home directory using *${LOGIN}* and
> *${USER}*.
>
> Environment variables may vary between Server APIs as those
> environments may be different.

**示例 \#3 Unix include\_path using ${USER} env variable**

``` php.ini
include_path = ".:${USER}/pear/php"
```

`open_basedir` <span class="type">string</span>  
Limit the files that can be accessed by PHP to the specified
directory-tree, including the file itself. This directive is *NOT*
affected by whether Safe Mode is turned On or Off.

When a script tries to access the filesystem, for example using <span
class="function">include</span>, or <span class="function">fopen</span>,
the location of the file is checked. When the file is outside the
specified directory-tree, PHP will refuse to access it. All symbolic
links are resolved, so it's not possible to avoid this restriction with
a symlink. If the file doesn't exist then the symlink couldn't be
resolved and the filename is compared to (a resolved) **open\_basedir**.

**open\_basedir** can affect more than just filesystem functions; for
example if *MySQL* is configured to use *mysqlnd* drivers, *LOAD DATA
INFILE* will be affected by **open\_basedir**. Much of the extended
functionality of PHP uses *open\_basedir* in this way.

The special value `.` indicates that the working directory of the script
will be used as the base-directory. This is, however, a little dangerous
as the working directory of the script can easily be changed with <span
class="function">chdir</span>.

In `httpd.conf`, **open\_basedir** can be turned off (e.g. for some
virtual hosts)
<a href="/configuration/changes.html#configuration.changes.apache" class="link">the same way</a>
as any other configuration directive with "*php\_admin\_value
open\_basedir none*".

Under Windows, separate the directories with a semicolon. On all other
systems, separate the directories with a colon. As an Apache module,
**open\_basedir** paths from parent directories are now automatically
inherited.

The restriction specified with **open\_basedir** is a directory name
since PHP 5.2.16 and 5.3.4. Previous versions used it as a prefix. This
means that "*open\_basedir = /dir/incl*" also allowed access to
"*/dir/include*" and "*/dir/incls*" if they exist. When you want to
restrict access to only the specified directory, end with a slash. For
example: *open\_basedir = /dir/incl/*

The default is to allow all files to be opened.

> **Note**:
>
> As of PHP 5.3.0 open\_basedir can be tightened at run-time. This means
> that if open\_basedir is set to */www/* in `php.ini` a script can
> tighten the configuration to */www/tmp/* at run-time with <span
> class="function">ini\_set</span>. When listing several directories,
> you can use the **`PATH_SEPARATOR`** constant as a separator
> regardless of the operating system.

> **Note**:
>
> Using open\_basedir will set
> <a href="/ini/core.html#ini.realpath-cache-size" class="link">realpath_cache_size</a>
> to *0* and thus *disable* the realpath cache.

`doc_root` <span class="type">string</span>  
PHP's "root directory" on the server. Only used if non-empty. If PHP is
configured with
<a href="/ini/sect/safe-mode.html#ini.safe-mode" class="link">安全模式</a>,
no files outside this directory are served. If PHP was not compiled with
FORCE\_REDIRECT, you *should* set doc\_root if you are running PHP as a
CGI under any web server (other than IIS). The alternative is to use the
<a href="/ini/core.html#ini.cgi.force-redirect" class="link">cgi.force_redirect</a>
configuration below.

`user_ini.cache_ttl` <span class="type">integer</span>  

`user_ini.filename` <span class="type">string</span>  

`user_dir` <span class="type">string</span>  
The base name of the directory used on a user's home directory for PHP
files, for example `public_html         `.

`extension_dir` <span class="type">string</span>  
In what directory PHP should look for dynamically loadable extensions.
See also: <a href="/info/setup.html#" class="link">enable_dl</a>, and
<span class="function">dl</span>.

`extension` <span class="type">string</span>  
Which dynamically loadable extensions to load when PHP starts up.

`zend_extension` <span class="type">string</span>  
Name of dynamically loadable Zend extension (for example
<a href="/book/apd.html" class="link">APD</a>) to load when PHP starts
up.

`zend_extension_debug` <span class="type">string</span>  
Variant of
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>
for extensions compiled with debug info prior to PHP 5.3.0.

`zend_extension_debug_ts` <span class="type">string</span>  
Variant of
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>
for extensions compiled with debug info and thread safety prior to PHP
5.3.0.

`zend_extension_ts` <span class="type">string</span>  
Variant of
<a href="/ini/core.html#ini.zend-extension" class="link">zend_extension</a>
for extensions compiled with thread safety prior to PHP 5.3.0.

`cgi.check_shebang_line` <span class="type">boolean</span>  
Controls whether CGI PHP checks for line starting with *\#!* (shebang)
at the top of the running script. This line might be needed if the
script support running both as stand-alone script and via PHP CGI. PHP
in CGI mode skips this line and ignores its content if this directive is
turned on.

`cgi.discard_path` <span class="type">boolean</span>  
If this is enabled, the PHP CGI binary can safely be placed outside of
the web tree and people will not be able to circumvent .htaccess
security.

`cgi.fix_pathinfo` <span class="type">boolean</span>  
Provides *real* *PATH\_INFO*/ *PATH\_TRANSLATED* support for CGI. PHP's
previous behaviour was to set *PATH\_TRANSLATED* to *SCRIPT\_FILENAME*,
and to not grok what *PATH\_INFO* is. For more information on
*PATH\_INFO*, see the CGI specs. Setting this to *1* will cause PHP CGI
to fix its paths to conform to the spec. A setting of zero causes PHP to
behave as before. It is turned on by default. You should fix your
scripts to use *SCRIPT\_FILENAME* rather than *PATH\_TRANSLATED*.

`cgi.force_redirect` <span class="type">boolean</span>  
cgi.force\_redirect is necessary to provide security running PHP as a
CGI under most web servers. Left undefined, PHP turns this on by
default. You can turn it off *at your own risk*.

> **Note**:
>
> Windows Users: When using IIS this option *must* be turned off. For
> OmniHTTPD or Xitami the same applies.

`cgi.nph` <span class="type">boolean</span>  
If cgi.nph is enabled it will force cgi to always sent Status: 200 with
every request.

`cgi.redirect_status_env` <span class="type">string</span>  
If cgi.force\_redirect is turned on, and you are not running under
Apache or Netscape (iPlanet) web servers, you *may* need to set an
environment variable name that PHP will look for to know it is OK to
continue execution.

> **Note**:
>
> Setting this variable *may* cause security issues, *know what you are
> doing first*.

`cgi.rfc2616_headers` <span class="type">int</span>  
Tells PHP what type of headers to use when sending HTTP response code.
If it's set to 0, PHP sends a
<a href="http://www.faqs.org/rfcs/rfc3875" class="link external">» RFC 3875</a>
"Status:" header that is supported by Apache and other web servers. When
this option is set to 1, PHP will send
<a href="http://www.faqs.org/rfcs/rfc2616" class="link external">» RFC 2616</a>
compliant headers.

If this option is enabled, and you are running PHP in a CGI environment
(e.g. PHP-FPM) you should not use standard RFC 2616 style HTTP status
response headers, you should instead use their RFC 3875 equivalent e.g.
instead of header("HTTP/1.0 404 Not found"); you should use
header("Status: 404 Not Found");

Leave it set to 0 unless you know what you're doing.

`fastcgi.impersonate` <span class="type">string</span>  
FastCGI under IIS (on WINNT based OS) supports the ability to
impersonate security tokens of the calling client. This allows IIS to
define the security context that the request runs under. mod\_fastcgi
under Apache does not currently support this feature (03/17/2002) Set to
1 if running under IIS. Default is zero.

`fastcgi.logging` <span class="type">boolean</span>  
Turns on SAPI logging when using FastCGI. Default is to enable logging.

File Uploads
------------

| 名字                                                                                  | 默认 | 可修改范围       | 更新日志                    |
|---------------------------------------------------------------------------------------|------|------------------|-----------------------------|
| <a href="/ini/core.html#ini.file-uploads" class="link">file_uploads</a>               | "1"  | PHP\_INI\_SYSTEM |                             |
| <a href="/ini/core.html#ini.upload-tmp-dir" class="link">upload_tmp_dir</a>           | NULL | PHP\_INI\_SYSTEM |                             |
| <a href="/info/setup.html#" class="link">max_input_nesting_level</a>                  | 64   | PHP\_INI\_PERDIR | Available since PHP 5.3.9.  |
| <a href="/info/setup.html#" class="link">max_input_vars</a>                           | 1000 | PHP\_INI\_PERDIR | Available since PHP 5.3.9.  |
| <a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a> | "2M" | PHP\_INI\_PERDIR |                             |
| <a href="/ini/core.html#ini.max-file-uploads" class="link">max_file_uploads</a>       | 20   | PHP\_INI\_SYSTEM | Available since PHP 5.2.12. |

这是配置指令的简短说明。

`file_uploads` <span class="type">boolean</span>  
Whether or not to allow HTTP
<a href="/features/file-upload.html" class="link">file uploads</a>. See
also the
<a href="/ini/core.html#ini.upload-max-filesize" class="link">upload_max_filesize</a>,
<a href="/ini/core.html#ini.upload-tmp-dir" class="link">upload_tmp_dir</a>,
and
<a href="/ini/core.html#ini.post-max-size" class="link">post_max_size</a>
directives.

`upload_tmp_dir` <span class="type">string</span>  
The temporary directory used for storing files when doing file upload.
Must be writable by whatever user PHP is running as. If not specified
PHP will use the system's default.

If the directory specified here is not writable, PHP falls back to the
system default temporary directory. If
<a href="/ini/core.html#ini.open-basedir" class="link">open_basedir</a>
is on, then the system default directory must be allowed for an upload
to succeed.

`upload_max_filesize` <span class="type">integer</span>  
The maximum size of an uploaded file.

<span class="simpara">当使用 <span class="type">integer</span> 时,
其值以字节来衡量。还可以使用在<a href="/faq/using.html#faq.using.shorthandbytes" class="link">FAQ</a>中描述的速记符。</span>

`max_file_uploads` <span class="type">integer</span>  
The maximum number of files allowed to be uploaded simultaneously.
Starting with PHP 5.3.4, upload fields left blank on submission do not
count towards this limit.

General SQL
-----------

| 名字                                                                      | 默认 | 可修改范围       | 更新日志             |
|---------------------------------------------------------------------------|------|------------------|----------------------|
| <a href="/ini/core.html#ini.sql.safe-mode" class="link">sql.safe_mode</a> | "0"  | PHP\_INI\_SYSTEM | Removed in PHP 7.2.0 |

这是配置指令的简短说明。

`sql.safe_mode` <span class="type">boolean</span>  
If turned on, database connection functions that specify default values
will use those values in place of any user-supplied arguments. For
details on the default values, see the documentation for the relevant
connection functions.

**Warning**
This feature has been *REMOVED* as of PHP 7.2.0.

Windows Specific
----------------

| 名字                                                                                            | 默认 | 可修改范围    | 更新日志                   |
|-------------------------------------------------------------------------------------------------|------|---------------|----------------------------|
| <a href="/ini/core.html#ini.windows-show-crt-warning" class="link">windows.show_crt_warning</a> | "0"  | PHP\_INI\_ALL | Available since PHP 5.4.0. |

这是配置指令的简短说明。

`windows.show_crt_warning` <span class="type">boolean</span>  
This directive shows the Windows CRT warnings when enabled. These
warnings were displayed by default until PHP 5.4.0.
