安装／配置
==========

**目录**

-   [需求](/xml/setup.html#需求)
-   [安装](/xml/setup.html#安装)
-   [运行时配置](/xml/setup.html#运行时配置)
-   [资源类型](/xml/setup.html#资源类型)

需求
----

此扩展需要 <a href="/book/libxml.html" class="link">libxml</a> PHP
扩展。这表示需要使用 **--enable-libxml**，尽管这将隐式完成因为 libxml
是缺省开启的。

缺省情况下，此扩展使用<span class="productname">expat compat layer
</span>。也可使用<span class="productname">expat</span>， 此库位于
<a href="http://www.jclark.com/xml/expat.html" class="link external">» http://www.jclark.com/xml/expat.html</a>。
使用<span class="productname">expat</span>库中的 Makefile
是不会默认构建出库文件的，可使用以下构建规则进行构建：

``` makefile
libexpat.a: $(OBJS)
    ar -rc $@ $(OBJS)
    ranlib $@
```

expat 的源代码 RPM 安装包可在
<a href="http://sourceforge.net/projects/expat/" class="link external">» http://sourceforge.net/projects/expat/</a>
找到。

安装
----

此扩展默认为启用,编译时可通过下列选项禁用： **--disable-xml**

这些函数默认为有效的，使用了捆绑的 expat 库。您可以通过参数
**--disable-xml** 来屏蔽 XML 的支持。如果您将 PHP 编译为 Apache 1.3.9
或更高版本的一个模块， PHP 将自动使用 Apache 捆绑的 <span
class="productname">expat</span> 库。如果您不希望使用该捆绑的 expat
库，请在运行 PHP 的 configure 配置脚本时使用参数
**--with-expat-dir=DIR**，其中 DIR 应该指向 expat 安装的根目录。

PHP 的 Windows
版本已内建对此扩展的支持。不需要载入额外的扩展来使用这些函数。

运行时配置
----------

此扩展没有在 `php.ini` 中定义配置指令。

资源类型
--------

<span class="function">xml\_parser\_create</span> 与 <span
class="function">xml\_parser\_create\_ns</span> 返回的 *XML* 资源会引用
XML 解析器实例，以被此扩展提供的函数使用。
