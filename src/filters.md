可用过滤器列表
==============

**目录**

-   [字符串过滤器](/filters/string.html)
-   [string.strip\_tags](/filters/string/strip_tags.html)
-   [转换过滤器](/filters/convert.html)
-   [压缩过滤器](/filters/compression.html)
-   [加密过滤器](/filters/encryption.html)

下面列出了用在 <span
class="function">stream\_filter\_append</span>中的几个内置的流过滤器。用户的
PHP 版本中的过滤器也许比这里列出的更多（或更少）。

值得指出 <span class="function">stream\_filter\_append</span>与 <span
class="function">stream\_filter\_prepend</span>之间有少许不平衡。每个
PHP 流都含有一个小的
*读取缓冲区*，它存储了来自文件系统或其它资源的几段数据以便更有效率地处理。数据一从资源进入流的内部缓冲区，立刻被附上的过滤器处理而不管
PHP 程序是否真的已经准备好接收数据。当过滤器是
*appended*时如果数据等待在读取缓冲区，数据将被立即通过过滤器处理，使其效果看上去是透明的。然而当过滤器是
*prepended*时如果数据等待在读取缓冲区，数据将
*不会*被该过滤器处理。该数据将会等到从资源取得下一段数据后才会被处理。

用 <span class="function">stream\_get\_filters</span>来列出 PHP
中已安装的过滤器。
