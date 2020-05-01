安装／配置
==========

**目录**

-   [需求](/yaml/setup.html#需求)
-   [安装](/yaml/setup.html#安装)
-   [运行时配置](/yaml/setup.html#运行时配置)
-   [资源类型](/yaml/setup.html#资源类型)

需求
----

This extension requires the
<a href="http://pyyaml.org/wiki/LibYAML" class="link external">» LibYAML C library</a>
version 0.1.0 or higher to be installed.

安装
----

此 <a href="https://pecl.php.net/" class="link external">» PECL</a>
扩展未与 PHP 捆绑。

安装此 PECL 扩展相关的信息可在手册中标题为
<a href="/install/pecl.html" class="link">PECL 扩展的安装</a>章节中找到。更多信息如新的发行版本、下载、源文件、
维护人员信息及变更日志等，都在此处：
<a href="https://pecl.php.net/package/yaml" class="link external">» https://pecl.php.net/package/yaml</a>.

运行时配置
----------

这些函数的行为受 `php.ini` 中的设置影响。

| 名字                                                               | 默认 | 可修改范围    | 更新日志                                       |
|--------------------------------------------------------------------|------|---------------|------------------------------------------------|
| <a href="/yaml/setup.html#" class="link">yaml.decode_binary</a>    | 0    | PHP\_INI\_ALL |                                                |
| <a href="/yaml/setup.html#" class="link">yaml.decode_php</a>       | 0    | PHP\_INI\_ALL | Added in 1.2.0, before 2.0.0 the default was 1 |
| <a href="/yaml/setup.html#" class="link">yaml.decode_timestamp</a> | 0    | PHP\_INI\_ALL |                                                |
| <a href="/yaml/setup.html#" class="link">yaml.output_canonical</a> | 0    | PHP\_INI\_ALL |                                                |
| <a href="/yaml/setup.html#" class="link">yaml.output_indent</a>    | 2    | PHP\_INI\_ALL |                                                |
| <a href="/yaml/setup.html#" class="link">yaml.output_width</a>     | 80   | PHP\_INI\_ALL |                                                |

这是配置指令的简短说明。

`yaml.decode_binary` <span class="type">boolean</span>  
Off by default, but can be set to on to cause base64 binary encoded
entities which have the explicit tag "tag:yaml.org,2002:binary" to be
decoded.

`yaml.decode_php` <span class="type">boolean</span>  
Off by default, but can be set to on to cause serialized php objects
which have the explicit tag "!php/object" to be unserialized.

`yaml.decode_timestamp` <span class="type">integer</span>  
Controls the decoding of both implicit and explicit
"tag:yaml.org,2002:timestamp" scalars in the YAML document stream. The
default setting of *0* will not apply any decoding. A setting of *1*
will use <span class="function">strtotime</span> to parse the timestamp
value as a Unix timestamp. A setting of *2* will use <span
class="function">date\_create</span> to parse the timestamp value as
<span class="type">DateTime</span> object.

`yaml.output_canonical` <span class="type">boolean</span>  
Off by default, but can be set to on to cause canonical form output.

`yaml.output_indent` <span class="type">integer</span>  
Number of spaces to indent sections. Value should be between *1* and
*10*.

`yaml.output_width` <span class="type">integer</span>  
Set the preferred line width. *-1* means unlimited.

资源类型
--------

此扩展没有定义资源类型。
