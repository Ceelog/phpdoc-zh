安装／配置
==========

**目录**

-   [需求](/soap/setup.html#需求)
-   [安装](/soap/setup.html#安装)
-   [运行时配置](/soap/setup.html#运行时配置)
-   [资源类型](/soap/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--with-libxml**，或在 PHP 7.4 之前的版本中使用
**--enable-libxml**， 尽管这将隐式完成因为 libxml 是缺省开启的。

安装
----

To enable SOAP support, configure PHP with **--enable-soap**.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                 | 默认  | 可修改范围    | 更新日志 |
|----------------------------------------------------------------------|-------|---------------|----------|
| <a href="/soap/setup.html#" class="link">soap.wsdl_cache_enabled</a> | 1     | PHP\_INI\_ALL |          |
| <a href="/soap/setup.html#" class="link">soap.wsdl_cache_dir</a>     | /tmp  | PHP\_INI\_ALL |          |
| <a href="/soap/setup.html#" class="link">soap.wsdl_cache_ttl</a>     | 86400 | PHP\_INI\_ALL |          |
| <a href="/soap/setup.html#" class="link">soap.wsdl_cache</a>         | 1     | PHP\_INI\_ALL |          |
| <a href="/soap/setup.html#" class="link">soap.wsdl_cache_limit</a>   | 5     | PHP\_INI\_ALL |          |

这是配置指令的简短说明。

`soap.wsdl_cache_enabled` <span class="type">integer</span>  
Enables or disables the WSDL caching feature.

`soap.wsdl_cache_dir` <span class="type">string</span>  
Sets the directory name where the SOAP extension will put cache files.

`soap.wsdl_cache_ttl` <span class="type">integer</span>  
Sets the number of seconds (time to live) that cached files will be used
instead of the originals.

`soap.wsdl_cache` <span class="type">integer</span>  
If `soap.wsdl_cache_enabled` is on, this setting determines the type of
caching. It can be any of: **`WSDL_CACHE_NONE`** (*0*),
**`WSDL_CACHE_DISK`** (*1*), **`WSDL_CACHE_MEMORY`** (*2*) or
**`WSDL_CACHE_BOTH`** (*3*). This can also be set via the `options`
array in the <span class="classname">SoapClient</span> or <span
class="classname">SoapServer</span> constructor.

`soap.wsdl_cache_limit` <span class="type">integer</span>  
Maximum number of in-memory cached WSDL files. Adding further files into
a full memory cache will delete the oldest files from it.

资源类型
--------

此扩展没有定义资源类型。
