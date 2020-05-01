PHP 扩展开发构建
----------------

在一个典型的 PHP
安装中，高性能的需要几乎总是造成以调试的便利为代价的优化。这是产品所使用的合理折衷方案，但当开发扩展时却达不到标准。
我们所需要的是 PHP 的安装包，以提示我们做什么事会出错。

Zend
引擎提供了一个内存管理器，有在扩展中跟踪内存泄漏的能力并提供详尽的调试信息。跟踪在默认情况下是被禁用的，同时也是线程安全的。要打开的话，应将
**--enable-debug** 和 *--enable-maintainer-zts*
选项与其他常用选项一起传给 `configure`。要获得从源代码构建 PHP
的说明，请看位于
<a href="/install/general.html" class="xref">安装前需要考虑的事项</a>
的说明。典型的 `configure` 命令行可能看起来象这样：

``` shell
$ ./configure --prefix=/where/to/install/php --enable-debug --enable-maintainer-zts --enable-cgi --enable-cli --with-mysql=/path/to/mysql
```
