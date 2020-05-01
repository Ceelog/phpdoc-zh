字符编码
========

PHP 的 XML 扩展通过几种不同的<span
class="glossterm">字符编码</span>支持<a href="http://www.unicode.org/" class="link external">» Unicode</a>
字符集。 有两类字符编码， <span class="glossterm">原始编码</span> 和
<span class="glossterm">目标编码</span>.
在PHP的内部展现中，文档始终是使用*UTF-8*编码。

当 XML 被 <a href="/ref/xml.html#xml_parse" class="link">解析</a>
后，原始编码就完成了。
在<a href="/ref/xml.html#xml_parser_create" class="link">创建 XML 解析器</a>时,
可以指定原始编码(在XML 解析器此后的生命周期里，不能修改此编码)。
被支持的原始编码有 *ISO-8859-1*, *US-ASCII* 和 *UTF-8*.
前两种是单字节编码, 即每一个字符表现为一个字节。 *UTF-8*
可将字符编码为一串不定数量(最高21)的位(bit), 排列成1到4个字节。 PHP
中使用的默认原始编码是*ISO-8859-1*.

当 PHP 将数据传给 XML 处理函数时，目标编码就完成了。 在创建 XML
处理器时，目标编码被设定为与原始编码相同，但可任意修改。
目标编码会影响字符数据及标签名，与处理指令目标。

如 XML 解析器遇到原始编码所能表示的范围之外的字符时，会返回一个错误。

如 PHP 遇到在被解析的 XML 文档中不能用所指定的目标编码表示的字符时，
这个问题字符会被“降级”。通常来说，就是那些字符会被替换成问号(?)。
