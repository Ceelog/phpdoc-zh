安装／配置
==========

**目录**

-   [需求](/imap/setup.html#需求)
-   [安装](/imap/setup.html#安装)
-   [运行时配置](/imap/setup.html#运行时配置)
-   [资源类型](/imap/setup.html#资源类型)

需求
----

This extension requires the c-client library to be installed. Grab the
latest version from
<a href="https://www.washington.edu/imap/" class="link external">» https://www.washington.edu/imap/</a>
and compile it.

It's important that you do not copy the IMAP source files directly into
the system include directory as there may be conflicts. Instead, create
a new directory inside the system include directory, such as
`/usr/local/imap-2000b/` (location and name depend on your setup and
IMAP version), and inside this new directory create additional
directories named `lib/` and `include/`. From the `c-client` directory
from your IMAP source tree, copy all the `*.h` files into `include/` and
all the `*.c` files into `lib/`. Additionally when you compiled IMAP, a
file named `c-client.a` was created. Also put this in the `lib/`
directory but rename it as `libc-client.a`.

> **Note**:
>
> To build the c-client library with SSL or/and Kerberos support read
> the docs supplied with the package.

> **Note**: <span class="simpara"> In Mandrake Linux, the IMAP library
> (`libc-client.a`) is compiled without Kerberos support. A separate
> version with SSL (`client-PHP4.a`) is installed. The library must be
> recompiled in order to add Kerberos support. </span>

安装
----

要使这些函数生效，你必须在编译 PHP 的时候添加 **--with-imap\[=DIR\]**
选项, DIR 表示c-client安装前缀。比如上面提到的例子中，你可以使用
**--with-imap=/usr/local/imap-2000b**.
根据以上描述，这个路径是指向你先前创建的文件夹。对于 <span
class="productname">Windows</span> 用户，应该在 `php.ini`
文件中引入`php_imap.dll`.

Windows 2000之前的系统是不支持的 IMAP
的。这是因为通过SSL连接邮件服务器时使用了加密功能。

> **Note**: <span class="simpara"> 因为取决于 c-client
> 是如何配置的，所以你应该向 PHP
> 配置行添加**--with-imap-ssl=/path/to/openssl/** 或者
> **--with-kerberos=/path/to/kerberos** 配置信息。 </span>

**Warning**

<a href="/book/imap.html" class="link">IMAP</a>，<a href="/book/recode.html" class="link">recode</a>，<a href="/book/yaz.html" class="link">YAZ</a>
和 <a href="/book/cyrus.html" class="link">Cyrus</a>
扩展不能同时使用，因为它们共享了相同 的内部符号。注意：Yaz 2.0
及以上版本不存在此问题。

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                  | 默认 | 可修改范围       | 更新日志                                                                           |
|-----------------------------------------------------------------------|------|------------------|------------------------------------------------------------------------------------|
| <a href="/imap/setup.html#" class="link">imap.enable_insecure_rsh</a> | "0"  | PHP\_INI\_SYSTEM | Available as of PHP 7.1.25, 7.2.13 and 7.3.0. Formerly, it was implicitly enabled. |

有关 PHP\_INI\_\* 样式的更多详情与定义，见
<a href="/configuration/changes/modes.html" class="xref">配置可被设定范围</a>。

这是配置指令的简短说明。

`imap.enable_insecure_rsh` <span class="type">boolean</span>  
Establishing a connection to a server may invoke **rsh** or **ssh**
commands, unless this `php.ini` option is disabled.

**Warning**
Neither PHP nor the IMAP library filter mailbox names before passing
them to **rsh** or **ssh** commands, thus passing untrusted data to this
function without disabling this `php.ini` option is *insecure*.

资源类型
--------

The *imap* resource as returned by <span
class="function">imap\_open</span> references an opened IMAP stream.
