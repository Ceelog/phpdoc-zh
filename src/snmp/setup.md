安装／配置
==========

**目录**

-   [需求](/snmp/setup.html#需求)
-   [安装](/snmp/setup.html#安装)
-   [运行时配置](/snmp/setup.html#运行时配置)
-   [资源类型](/snmp/setup.html#资源类型)

需求
----

In order to use the SNMP functions requires installation of the
<a href="http://www.net-snmp.org/" class="link external">» Net-SNMP</a>
package. SNMPv3 functions available only when
<a href="http://www.openssl.org/" class="link external">» OpenSSL</a>
package is installed too.

Net-SNMP version 5.3+ is required for Unix installations and Net-SNMP
version 5.4+ for Windows.

安装
----

重要提示：为了使用 UCD SNMP 包，需要在编译之前将
*NO\_ZEROLENGTH\_COMMUNITY* 定义为 *1*。 在配置 UCD SNMP 之后，编辑
`config.h` 或 `acconfig.h`，查找 *NO\_ZEROLENGTH\_COMMUNITY*，将
\#define 所在行的注释去掉。修改后应该类似这样：

``` c
#define NO_ZEROLENGTH_COMMUNITY 1
```

然后使用 **--with-snmp\[=DIR\]** 选项编译 PHP。

如果在组合 SNMP
命令时看到奇怪的字段错误，那就是因为没有遵从上述说明。如果不想重新编译
UCD SNMP，可以使用 **--enable-ucd-snmp-hack** 开关编译 PHP
以绕开上述错误。

Windows 版本在目录 `mibs` 中包含了支持 SNMP 的文件。此目录应该移到
`DRIVE:\usr\mibs`，其中 DRIVE 是安装 PHP 所在的盘符，例如
`c:\usr\mibs`。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

此扩展没有定义资源类型。
