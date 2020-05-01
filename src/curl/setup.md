安装／配置
==========

**目录**

-   [需求](/curl/setup.html#需求)
-   [安装](/curl/setup.html#安装)
-   [运行时配置](/curl/setup.html#运行时配置)
-   [资源类型](/curl/setup.html#资源类型)

需求
----

需要安装<a href="http://curl.haxx.se/" class="link external">» libcurl</a>包才能使用
PHP 的 cURL 函数。PHP 需要使用 7.10.5 或更高版本的 libcurl。

安装
----

要 PHP 支持 cURL，必须在编译 PHP 时加上 **--with-curl\[=DIR\]**
选项，DIR 为包含 `lib` 和 `include` 的目录路径。在 `include`
目录中必须有一个名为`curl`，包含了`easy.h` 和`curl.h`
的文件夹。`lib`文件夹里应该有一个名为`libcurl.a`的文件。对于 PHP 4.3.0
你可以配置 **--with-curlwrappers** 使 cURL 使用 URL 流。

> **Note**: **Win32 用户注意**  
> <span class="simpara"> 要在 Windows 环境下使用这个模块，`libeay32.dll`
> 和 `ssleay32.dll` 必须放到 PATH 环境变量包含的目录下。 </span> <span
> class="simpara"> 不用 cURL 网站上的`libcurl.dll`。 </span>

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                     | 默认 | 可修改范围       | 更新日志             |
|----------------------------------------------------------|------|------------------|----------------------|
| <a href="/curl/setup.html#" class="link">curl.cainfo</a> | NULL | PHP\_INI\_SYSTEM | 自 PHP 5.3.7. 起有效 |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`curl.cainfo` <span class="type">string</span>  
**`CURLOPT_CAINFO`** 选项的一个默认值。这个值必须是一个绝对路径。

资源类型
--------

这个扩展定义了2种资源：cURL 句柄和 cURL 批处理句柄。
