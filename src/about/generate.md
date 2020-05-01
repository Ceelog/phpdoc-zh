如何生成手册的各种格式
----------------------

本手册使用 XML 语言编写，同时运用了
<a href="http://www.oasis-open.org/docbook/xml/" class="link external">» DocBook XML DTD</a>。还用了
<a href="https://wiki.php.net/doc/phd/" class="link external">» PhD</a>（基于
\[PH\]P 的 \[D\]ocBook 渲染器）来维护和格式化。

将 XML
语言作为源文件格式，使得我们只需维护该源文件文档，就可以可以利用它生成许多其它的输出格式。生在在线手册格式的工具是
<a href="https://wiki.php.net/doc/phd/" class="link external">» PhD</a>。我们使用
<a href="http://msdn.microsoft.com/library/en-us/htmlhelp/html/vsconhh1start.asp" class="link external">» Microsoft HTML Help Workshop</a>
来生成本手册的 <span class="productname">Windows HTML 帮助</span>
格式。当然，PHP 本身也完成了其它一些转换和格式化工作。

PHP 手册被生成多种不同语言和格式，详情见
<a href="https://www.php.net/docs.php" class="link external">» https://www.php.net/docs.php</a>。XML
格式的源代码可以通过 SVN 下载，并通过
<a href="https://svn.php.net/viewvc/" class="link external">» https://svn.php.net/viewvc/</a>
在线浏览。文档存放于 *phpdoc* 模块中。
