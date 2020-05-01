安装／配置
==========

**目录**

-   [运行时配置](/phpdbg/setup.html#运行时配置)

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                       | 默认 | 可修改范围    | 更新日志                  |
|------------------------------------------------------------|------|---------------|---------------------------|
| <a href="/phpdbg/setup.html#" class="link">phpdbg.eol</a>  | 2    | PHP\_INI\_ALL | Available as of PHP 7.0.0 |
| <a href="/phpdbg/setup.html#" class="link">phpdbg.path</a> |      | 6             | Available as of PHP 5.6.3 |

这是配置指令的简短说明。

`phpdbg.eol` <span class="type">mixed</span>  
The kind of line ending to use for output. For setting the value, one of
the string aliases must be used.

| <span class="type">int</span> Value | <span class="type">string</span> Alias |
|-------------------------------------|----------------------------------------|
| *0*                                 | *CRLF*, *crlf*, *DOS*, *dos*           |
| *1*                                 | *LF*, *lf*, *UNIX*, *unix*             |
| *2*                                 | *CR*, *cr*, *MAC*, *mac*               |

`phpdbg.path` <span class="type">string</span>  
