安装／配置
==========

**目录**

-   [需求](/trader/setup.html#需求)
-   [安装](/trader/setup.html#安装)
-   [运行时配置](/trader/setup.html#运行时配置)

需求
----

The trader extension is based on
<a href="http://www.ta-lib.org/" class="link external">» TA-Lib</a>.
TA-Lib is fully integrated into the extension, therefore no external
libraries are needed.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/trader" class="link external">» https://pecl.php.net/package/trader</a>.

A DLL for this PECL extension is available under
<a href="http://windows.php.net/downloads/pecl/releases/trader/" class="link external">» http://windows.php.net/downloads/pecl/releases/trader/</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                                  | 默认       | 可修改范围    | 更新日志           |
|-----------------------------------------------------------------------|------------|---------------|--------------------|
| <a href="/trader/setup.html#" class="link">trader.real_precision</a>  | 3          | PHP\_INI\_ALL | Since trader 0.2.1 |
| <a href="/trader/setup.html#" class="link">trader.real_round_mode</a> | HALF\_DOWN | PHP\_INI\_ALL | Since trader 0.3.0 |

这是配置指令的简短说明。

`trader.real_precision` <span class="type">integer</span>  
All the values in the returned arrays will be rounded to this precision.
However the calculations inside TA-Lib happen with unrounded values.

`trader.real_round_mode` <span class="type">string</span>  
Controls the trader real rounding policy. Valid values are *HALF\_UP*,
*HALF\_DOWN*, *HALF\_EVEN* and *HALF\_ODD*. The behaviour is identical
to the <a href="/ref/math.html#round" class="link">round()</a> function
used with the mode argument.
