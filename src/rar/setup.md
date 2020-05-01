安装／配置
==========

**目录**

-   [需求](/rar/setup.html#需求)
-   [安装](/rar/setup.html#安装)
-   [运行时配置](/rar/setup.html#运行时配置)
-   [资源类型](/rar/setup.html#资源类型)

需求
----

构建此扩展不需要其他扩展。

安装
----

Rar is currently available through PECL
<a href="https://pecl.php.net/package/rar" class="link external">» https://pecl.php.net/package/rar</a>.

Also you can use the PECL installer to install the Rar extension, using
the following command: **pecl -v install rar**.

You can always download the `tar.gz` package and install Rar by hand:

**示例 \#1 Rar installation**

``` shell
gunzip rar-xxx.tgz
tar -xvf rar-xxx.tar
cd rar-xxx
phpize
./configure && make && make install
```

Windows users will enable `php_rar.dll` inside of `php.ini` in order to
use these functions. PECL 扩展的 DLL 当前不可用。参见
<a href="/install/windows/legacy/index.html#install.windows.building" class="link">在 Windows 上构建</a>章节。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

This extension registers three internal classes: The archive
representations returned by <span class="function">rar\_open</span> –
<span class="type">RarArchive</span> –, the entry representations
returned by <span class="function">rar\_list</span> and <span
class="function">rar\_entry\_get</span> – <span
class="type">RarEntry</span> and the exception type <span
class="type">RarException</span>.

This extension also register a stream resource, called "rar" and a URL
wrapper called "rar wrapper" and registered under the prefix "rar".
